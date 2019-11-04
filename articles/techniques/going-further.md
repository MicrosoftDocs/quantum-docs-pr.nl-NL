---
title: 'Q # technieken-verder gaan | Microsoft Docs'
description: 'Q # technieken-verder gaan'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4677b0f9c4f64a9c1bc46d34e8a883dc006ba8f0
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183298"
---
# <a name="going-further"></a>Verder gaan #

Nu u hebt gezien hoe u interessante Quantum Programma's schrijft in Q #, gaat u naar deze sectie voor meer informatie over een aantal geavanceerde onderwerpen die nuttig moeten worden behandeld.

<!-- Moved Debugging and Testing Quantum Programs section to a separate article -->

## <a name="generic-operations-and-functions"></a>Algemene bewerkingen en functies ##

> [!TIP]
> In deze sectie wordt ervan uitgegaan dat u bekend bent met [algemene C# ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics)kennis in, [generieke F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [ C++ sjablonen](https://docs.microsoft.com/cpp/cpp/templates-cpp)of soort gelijke benaderingen voor het Program meren in andere talen.

Veel functies en bewerkingen die u mogelijk wilt definiëren, zijn niet echt afhankelijk van de typen invoer, maar u kunt de typen echter alleen impliciet gebruiken via een andere functie of bewerking.
Stel dat het *kaart* concept gebruikelijk is in veel functionele talen. met een functie $f (x) $ en een verzameling waarden $\{x_1, x_2, \dots, x_n\}$, kaart retourneert een nieuwe verzameling $\{f (x_1), f (x_2), \dots, f (x_n)\}$.
Om dit in Q # te implementeren, kunnen we profiteren van die functies de eerste klasse.
We gaan een snel voor beeld van `Map`schrijven, met behulp van ★ als tijdelijke aanduiding, terwijl we weten welke typen we nodig hebben.

```qsharp
function Map(fn : ★ -> ★, values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Houd er rekening mee dat deze functie veel hetzelfde lijkt, ongeacht de werkelijke typen die we vervangen.
Een kaart van gehele getallen tot Paulis, bijvoorbeeld ziet er ongeveer hetzelfde uit als een kaart van drijvende-komma getallen naar teken reeksen:

```qsharp
function MapIntsToPaulis(fn : Int -> Pauli, values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : Double -> String, values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

In principe kunnen we een versie van `Map` schrijven voor elk paar typen dat we tegen komen, maar dit heeft een aantal problemen.
Als we bijvoorbeeld een bug in `Map`vinden, moeten we ervoor zorgen dat de oplossing op uniforme wijze wordt toegepast in alle versies van `Map`.
Als we een nieuwe tuple of UDT bouwen, moeten we nu ook een nieuwe `Map` maken om samen met het nieuwe type te gaan.
Hoewel dit kan worden ondervangen voor een klein aantal dergelijke functies, omdat we meer en meer functies van hetzelfde formulier verzamelen als `Map`, zijn de kosten van het introduceren van nieuwe typen onredelijk groot in redelijk korte volg orde.

Veel van deze problemen kunnen er echter toe leiden dat de informatie die nodig is om te bepalen hoe de verschillende versies van `Map` zijn gerelateerd, niet aan de compiler is gegeven.
We willen het compileren om `Map` te behandelen als een soort wiskundige functie van Q #- *typen* tot q #-functies.
Dit principe wordt formeel door het toestaan van functies en bewerkingen om *type parameters*te hebben, evenals de normale tuple-para meters.
In de bovenstaande voor beelden willen we `Map` zien als having-para meters `Int, Pauli` in het eerste geval en `Double, String` in het tweede geval.
In het algemeen kunnen deze type parameters vervolgens worden gebruikt alsof het normale typen zijn: we gebruiken waarden van het type para meters om matrices en Tuples te maken, functies en bewerkingen aan te roepen en toe te wijzen aan gewone of onveranderlijke variabelen.

> [!NOTE]
> Het meest extreme geval van indirecte afhankelijkheid is die van qubits, waarbij een Q #-programma niet rechtstreeks kan vertrouwen op de structuur van het `Qubit` type, maar **moet** dergelijke typen door geven aan andere bewerkingen en functies.

Als u terugkeert naar bovenstaand voor beeld, kunnen we zien dat `Map` over de type parameters moet beschikken, een voor de invoer van `fn` en één om de uitvoer van `fn`weer te geven.
In Q # wordt dit geschreven door punt haken toe te voegen (dat is `<>`, niet brakets $ \braket{}$!) na de naam van een functie of bewerking in de declaratie ervan en door elk type para meter te vermelden.
De naam van elke type parameter moet beginnen met een Tick `'`, wat aangeeft dat het een type parameter is en niet een gewoon type (ook wel een *concreet* type genoemd).
Voor `Map`kunnen we het volgende schrijven:

```qsharp
function Map<'Input, 'Output>(fn : 'Input -> 'Output, values : 'Input[]) : 'Output {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Houd er rekening mee dat de definitie van `Map<'Input, 'Output>` erg lijkt op de versies die we eerder hebben afgeschreven.
Het enige verschil is dat we de compiler expliciet hebben geïnformeerd dat `Map` niet rechtstreeks afhankelijk is van wat `'Input` en `'Output` zijn, maar voor elk van beide typen indirect via `fn`.
Zodra we `Map<'Input, 'Output>` op deze manier hebben gedefinieerd, kunnen we deze aanroepen alsof het een gewone functie was:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Het schrijven van algemene functies en bewerkingen is een plek waar ' tuple-in ' tuple-out ' een zeer handige manier is om te denken over Q #-functies en-bewerkingen.
> Omdat elke functie precies één invoer heeft en er precies één uitvoer wordt geretourneerd, wordt een invoer van het type `'T -> 'U` overeenkomt met *een* Q #-functie.
> Op dezelfde manier kan elke bewerking worden door gegeven aan een invoer van het type `'T => 'U`.

Als tweede voor beeld moet u de uitdaging van het schrijven van een functie die de samen stelling van twee andere functies retourneert, overwegen:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier moeten we precies opgeven wat `A`, `B`en `C` zijn, waardoor het hulp programma van onze nieuwe `Compose` functie aanzienlijk wordt beperkt.
Na alle is `Compose` alleen afhankelijk van `A`, `B`en `C` *via* `innerFn` en `outerFn`.
Als alternatief kunnen we type parameters toevoegen aan `Compose` die aangeven dat het werkt voor *alle* `A`, `B`en `C`, zolang deze para meters overeenkomen met die van `innerFn` en `outerFn`:

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

De standaard bibliotheken van Q # bieden een reeks dergelijke bewerkingen en functies van type para meters waarmee de controle stroom van een hogere volg orde eenvoudiger kan worden gemaakt.
Deze worden verder besproken in de [hand leiding Q # Standard Library](xref:microsoft.quantum.libraries.standard.intro).

## <a name="borrowing-qubits"></a>Lenende qubits ##

Met het lenende mechanisme kunt u de toewijzing van qubits die als Scratch ruimte kan worden gebruikt tijdens een berekening. Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket{0}$. Een van de ' Dirty ' qubits als hun status is onbekend en kan zelfs worden Entangled met andere delen van het geheugen van de quantum computer. In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.

In de Canon zijn voor beelden die gebruikmaken van het sleutel woord `borrowing`, bijvoorbeeld de functie `MultiControlledXBorrow` hieronder gedefinieerd.
Als `controls` het besturings element qubits dat moet worden toegevoegd aan een `X` bewerking, wordt er in het algemeen `Length(controls)-2` veel vuil ancillas toegevoegd door deze implementatie.

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

Houd er rekening mee dat uitgebreid gebruik van de `With` Combinator---in het formulier dat van toepassing is op bewerkingen die ondersteuning bieden voor adjoint, dat wil zeggen, `WithA`---is gemaakt in dit voor `With` beeld. het besturings element wordt door gegeven aan de binnenste bewerking. Naast de `body` van de bewerking is een implementatie van de `controlled` hoofd tekst van de bewerking expliciet gegeven, in plaats van een `controlled auto`-instructie te gebruiken. De reden hiervoor is dat we van de structuur van het circuit weten hoe u gemakkelijk verdere controles kunt toevoegen die nuttig zijn voor het toevoegen van controle aan elke afzonderlijke poort in de `body`. 

Het is een goed proces om deze code te vergelijken met een andere Canon-functie `MultiControlledXClean` die hetzelfde doel heeft als het implementeren van een met vermenigvuldiging beheerde `X`-bewerking, die gebruikmaakt van verschillende schone qubits met behulp van het `using`-mechanisme. 
