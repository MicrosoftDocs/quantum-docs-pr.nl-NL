---
title: 'Q # bestands structuur'
description: "Meer informatie over het structureren van naam ruimten, en bewerkingen, functies en door de gebruiker gedefinieerde type declaraties in Q # Program ma's en bibliotheken."
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 96de062bc6ce4edf94520bec449e8d95259c0f5c
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320759"
---
# <a name="file-structure"></a>Bestandsstructuur

Een Q #-bestand bestaat uit een reeks naam ruimte declaraties.
Elke naam ruimte declaratie bevat declaraties voor door de gebruiker gedefinieerde typen, bewerkingen en functies.
Een naam ruimte declaratie kan elk wille keurig aantal van elk type declaratie en in een wille keurige volg orde bevatten.
De enige tekst die buiten een naam ruimte declaratie kan worden weer gegeven, is opmerkingen.
In het bijzonder worden documentatie opmerkingen voor een naam ruimte voorafgaat aan de declaratie.

## <a name="namespace-declarations"></a>Naam ruimte declaraties

Een Q #-bestand heeft normaal gesp roken precies één naam ruimte declaratie, maar kan geen hebben (en mag niet leeg zijn of alleen opmerkingen bevatten) of kan meerdere naam ruimten bevatten.
Naam ruimte declaraties mogen niet worden genest.

Dezelfde naam ruimte kan worden gedeclareerd in meerdere Q #-bestanden die samen worden gecompileerd, zolang er geen type, bewerking of functie declaraties met dezelfde naam zijn.
Het is met name ongeldig om hetzelfde type in dezelfde naam ruimte in meerdere bestanden te definiëren, zelfs als de declaraties identiek zijn.

Een naam ruimte declaratie bestaat uit het tref woord `namespace`, gevolgd door de naam van de naam ruimte, een open accolade `{`, de declaraties in de naam ruimte en een sluitende accolade `}`.
Naam ruimte namen volgen het .NET-patroon van een reeks van een of meer juridische symbolen, gescheiden door punten `.`.
Zo zijn `MyQuantumStuff` en `Microsoft.Quantum.Canon` geldige naam ruimte namen.
Per Conventie worden de symbolen in de naam van een naam ruimte gekapitaliseerd, maar dit is niet vereist.

Declaraties kunnen in een wille keurige volg orde worden weer gegeven in een naam ruimte declaratie.
Verwijzingen naar typen of callables die verder in een bestand worden aangegeven, worden op de juiste wijze opgelost. het is niet nodig om een verwijzing naar het type, de bewerking of de functie te gebruiken.

## <a name="open-directives"></a>Open instructies

Binnen een naam ruimte blok kan de `open`-instructie worden gebruikt voor het importeren van alle typen en callables die in een bepaalde naam ruimte zijn gedefinieerd en deze te raadplegen op basis van de niet-gekwalificeerde naam. 

Een dergelijke `open`-instructie bestaat uit het sleutel woord `open`, gevolgd door de naam ruimte die moet worden geopend en een punt komma als scheidings tekens.

Bijvoorbeeld,

```qsharp
open Microsoft.Quantum.Canon;
```

Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam. Een dergelijke korte naam wordt gedefinieerd door het tref woord `as` gevolgd door de gewenste korte naam vóór de punt komma in een `open`-instructie toe te voegen:

```qsharp
open Microsoft.Quantum.Math as Math;
```

Alle `open`-instructies moeten vóór een `function`, `operation`of `newtype` declaraties in het naam ruimte blok worden weer gegeven.
De `open`-instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.

## <a name="user-defined-type-declarations"></a>Door de gebruiker gedefinieerde type declaraties

Q # biedt gebruikers een manier om nieuwe door de gebruiker gedefinieerde typen te declareren, zoals beschreven in de sectie [Q # type model](xref:microsoft.quantum.language.type-model) .
Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.
In het bijzonder is er geen automatische conversie tussen waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.

Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype`, gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=`, een geldige type specificatie en een afsluitende punt komma.

Bijvoorbeeld:

```qsharp
newtype PairOfInts = (Int, Int);
```

Elk Q #-bron bestand kan elk gewenst aantal door de gebruiker gedefinieerde typen declareren.
Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.

Het is niet mogelijk om circulaire afhankelijkheden tussen door de gebruiker gedefinieerde typen te definiëren. Recursieve typen zijn daarom niet mogelijk binnen Q #.

## <a name="operation-declarations"></a>Bewerkings declaraties

Bewerkingen zijn de kern van Q #, ongeveer vergelijkbaar met functies in andere talen.
Elk Q #-bron bestand kan een wille keurig aantal bewerkingen definiëren.

Bewerkings namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met type-en functie namen.

Een bewerkings declaratie bestaat uit het tref woord `operation`, gevolgd door het symbool dat de naam van de bewerking is, een getypte id-tuple waarmee de argumenten voor de bewerking worden gedefinieerd, een dubbele punt `:`, een type aantekening waarmee het resultaat type van de bewerking wordt beschreven, optioneel een aantekening met de bewerkings kenmerken, een open accolade `{`, de hoofd `}`tekst

De hoofd tekst van de bewerkings declaratie bestaat uit de standaard implementatie of van een lijst met specials.
De standaard implementatie kan rechtstreeks in de declaratie worden opgegeven als alleen de implementatie van de standaard hoofd code specialize expliciet moet worden opgegeven.
In dit geval is een aantekening met de bewerkings kenmerken in de declaratie handig om ervoor te zorgen dat de compiler automatisch andere specials wordt gegenereerd op basis van de standaard implementatie. 

Bijvoorbeeld 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

Met bewerkings kenmerken wordt gedefinieerd welke soorten functors kunnen worden toegepast op de gedeclareerde bewerking en welk effect ze hebben. Als een bewerking een unitary-trans formatie implementeert, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt.
Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking. De bijbehorende implementatie voor elke impliciet gedeclareerde specialisatie wordt vervolgens door de compiler gegenereerd. In het bovenstaande voor beeld worden een adjoint, een beheerde en beheerde adjoint-specialisatie gegenereerd door de compiler. 

Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven. Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte generatie-instructie die verduidelijkt hoe een bepaalde specialisatie moet worden gebouwd of een door de gebruiker gedefinieerde implementatie. De code in `PrepareEntangledPair` hierboven is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
Het sleutel woord `auto` geeft aan dat de compiler moet bepalen hoe u de implementatie van de specialisatie wilt genereren.
Als de compiler de implementatie voor een bepaalde specialisatie niet kan genereren zonder verdere instructies, zoals een nauw keurigere generatie-instructie, of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```

In het bovenstaande voor beeld geeft `adjoint invert;` aan dat de adjoint-specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie te omkeren.

Voor een bewerking ter ondersteuning van de toepassing van de `Adjoint` en/of `Controlled` functor moet het retour type per se worden `Unit`. 


### <a name="explicit-specialization-declarations"></a>Expliciete specialisatie declaraties

Q #-bewerkingen kunnen de volgende expliciete specialisatie declaraties bevatten:

- Met de `body` specialize wordt de implementatie van de bewerking opgegeven waarvoor geen functors is toegepast.
- Met de `adjoint` specialize wordt de implementatie van de bewerking opgegeven waarop de `Adjoint` functor is toegepast.
- Met de `controlled` specialize wordt de implementatie van de bewerking opgegeven waarop de `Controlled` functor is toegepast.
- Met de `controlled adjoint` specialize wordt de implementatie van de bewerking opgegeven met zowel de `Adjoint` als `Controlled` functors toegepast.
  Deze specialisatie kan ook worden benoemd `adjoint controlled`, omdat de twee functors werkend zijn.


Een specialisatie bewerking bestaat uit de code voor specialisatie (zoals bijvoorbeeld `body`of `adjoint`enzovoort), gevolgd door een van de volgende opties:

- Een expliciete declaratie zoals hieronder wordt beschreven.
- Een instructie die de compiler vertelt hoe de specialisatie moet worden gegenereerd, een van de volgende opties:
  - `intrinsic`, wat aangeeft dat de specialisatie wordt verschaft door de doel computer.
  - `distribute`, die kan worden gebruikt met de `controlled` en `controlled adjoint` specials.
    Bij gebruik in combi natie met `controlled`geeft het aan dat de compiler de specialisatie moet berekenen door `Controlled` toe te passen op alle bewerkingen in de `body`.
    Bij gebruik in combi natie met `controlled adjoint`geeft het aan dat de compiler de specialisatie moet berekenen door `Controlled` toe te passen op alle bewerkingen in de `adjoint` specialisatie.
  - `invert`, wat aangeeft dat de compiler de `adjoint` specialisatie moet berekenen door de `body`te omkeren, dat wil zeggen de volg orde van de bewerkingen en het Toep assen van de adjoint.
    In combi natie met `adjoint controlled`geeft dit aan dat de compiler de specialisatie moet berekenen door de `controlled` specialisatie te omkeren.
  - `self`, om aan te geven dat de adjoint specialize hetzelfde is als de `body` specialize.
    Dit is juridisch voor de `adjoint` en `adjoint controlled` specials.
    Voor `adjoint controlled`impliceert `self` dat de `adjoint controlled` specialize hetzelfde is als de specialisatie `controlled`.
  - `auto`, om aan te geven dat de compiler een geschikte richt lijn moet selecteren om toe te passen.
    `auto` mag niet worden gebruikt voor de `body` specialize.

De instructies en `auto` alle vereisen een sluitende punt komma `;`.
De `auto`-instructie wordt omgezet in de volgende generatie-instructie als een expliciete declaratie van de `body` wordt gegeven:

- De `adjoint` specialisatie wordt gegenereerd volgens de richt lijn `invert`.
- De `controlled` specialisatie wordt gegenereerd volgens de richt lijn `distribute`.
- De `adjoint controlled` specialisatie wordt gegenereerd volgens de richt lijn `invert` als een expliciete declaratie voor `controlled` wordt gegeven, maar niet een voor `adjoint`, en `distribute` anders.

> [!TIP]   
> Als een bewerking zelf adjoint is, geeft u expliciet de adjoint of de bewaakte adjoint-specialisatie op via de generatie-instructie `self` zodat de compiler gebruik kan maken van die gegevens voor optimaliserings doeleinden.

Een specialisatie declaratie met een door de gebruiker gedefinieerde implementatie bestaat uit een argument tuple gevolgd door een instructie blok met de Q #-code die de specialisatie implementeert.
In de lijst met argumenten wordt `...` gebruikt om de argumenten weer te geven die zijn gedeclareerd voor de bewerking als geheel.
Voor `body` en `adjoint`moet de lijst met argumenten altijd worden `(...)`; voor `controlled` en `adjoint controlled`moet de lijst met argumenten een symbool zijn dat de matrix van besturings element qubits, gevolgd door `...`, tussen haakjes. bijvoorbeeld `(controls,...)`.

Als een of meer specialisaties naast de standaard hoofd tekst expliciet moeten worden gedeclareerd, moet de implementatie voor de standaard hoofd tekst ook worden ingepakt in een geschikte specialisatie declaratie.

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="adjoint"></a>Adjoint

Met de adjoint van een bewerking wordt aangegeven hoe de complexe geconjugeerde van de bewerking wordt geïmplementeerd, dat wil zeggen hoe de bewerking optreedt als ' in omgekeerde volg orde ' wordt uitgevoerd.
Het is wettelijk om een bewerking zonder adjoint op te geven. meting bewerkingen hebben bijvoorbeeld geen adjoint, omdat ze niet omkeerbaar zijn.
Een bewerking ondersteunt de `Adjoint` functor als de bijbehorende declaratie een impliciete of expliciete declaratie van een adjoint specialize bevat.
Een expliciet gedeclareerde beheerde adjoint specialisatie impliceert dat er een adjoint-specialisatie bestaat. 

Voor een bewerking waarvan de hoofd tekst herhalen-tot-succes-lussen bevat, stelt u instructies, metingen, retour overzichten of aanroepen naar andere bewerkingen die de `Adjoint` functor niet ondersteunen, het automatisch genereren van een adjoint-specialisatie volgens de `invert` of `auto`-instructie is niet mogelijk.

### <a name="controlled"></a>Gelijkrichter

Met de gecontroleerde versie van een bewerking wordt aangegeven hoe een door een Quantum beheerde versie van de bewerking wordt geïmplementeerd, d.w.z. hoe een bewerking reageert wanneer deze wordt toegepast op de status van een Quantum register.
Een gedetailleerde beschrijving vindt u in de sectie [Controlled](xref:microsoft.quantum.language.type-model#controlled) .

Het is wettelijk om een bewerking zonder gecontroleerde versie op te geven. meting bewerkingen hebben bijvoorbeeld geen beheerde versie, omdat ze niet kunnen worden beheerd.
Een bewerking ondersteunt de `Controlled` functor indien en alleen als de declaratie ervan een impliciete of expliciete declaratie van een beheerde specialisatie bevat.
Een expliciet gedeclareerde beheerde adjoint specialisatie impliceert dat er een beheerde specialisatie bestaat. 

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen ondersteuning bieden voor de `Controlled` functor, wordt het automatisch genereren van een gecontroleerde specialisatie volgens de `distribute` of `auto`-instructie niet mogelijk.

### <a name="controlled-adjoint"></a>Beheerde adjoint

De gecontroleerde adjoint-versie van een bewerking geeft aan hoe een Quantum versie van de adjoint van de bewerking wordt geïmplementeerd.
Het is niet toegestaan een bewerking op te geven zonder beheerde adjoint-versie. meting bewerkingen hebben bijvoorbeeld geen beheerde adjoint-versie omdat ze niet kunnen worden ingesteld of omkeerbaar.

Een beheerde adjoint-specialisatie voor een bewerking moet bestaan als en alleen als zowel een adjoint als een beheerde specialisatie bestaan. In dat geval wordt het bestaan van de beheerde adjoint-specialisatie afgeleid en wordt er een geschikte specialisatie gegenereerd door de compiler als er expliciet geen implementatie is gedefinieerd. 

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen beheerde adjoint-versie hebben, kunt u het automatisch genereren van een adjoint-specialisatie volgens de `invert`, `distribute` of `auto`-instructie niet mogelijk is.


### <a name="examples"></a>Voorbeelden

Een bewerkings declaratie kan zo eenvoudig zijn als het volgende, wat de primitieve Pauli X-bewerking definieert:

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

Het volgende definieert de bewerking teleporteer.

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation PrepareEntangledPair (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        PrepareEntangledPair(target, ancilla);

        // Do the teleportation
        Adjoint PrepareEntangledPair(ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a>Functie declaraties

Functions zijn louter klassieke routines in Q #.
Elk Q #-bron bestand kan een wille keurig aantal functies definiëren.

Een functie declaratie bestaat uit het tref woord `function`, gevolgd door het symbool dat de naam van de functie, een getypeerde id-tupel, een type aantekening is die het retour type van de functie beschrijft, en een instructie blok waarmee de implementatie van de functie wordt beschreven.

Het instructie blok dat een functie definieert, moet zijn Inge sloten in `{` en `}` als een ander instructie blok.

Functie namen moeten uniek zijn binnen een naam ruimte en kunnen een conflict veroorzaken met bewerkingen en type namen.
Functies mogen geen qubits toewijzen of lenen, of aanroepen. Gedeeltelijke toepassing van bewerkingen of het door geven van getypte waarden is nauw keurig.

Bijvoorbeeld:

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```


## <a name="internal-declarations"></a>Interne declaraties

Door de gebruiker gedefinieerde typen, bewerkingen en functies kunnen ook worden gedeclareerd als *intern*.
Dit betekent dat ze alleen kunnen worden geopend vanuit het Q #-project waarin ze zijn gedeclareerd.
Wanneer een project wordt gebruikt als referentie, worden alle *open bare* (niet-interne) declaraties beschikbaar gesteld, maar bij het gebruik van een interne declaratie van een ander project wordt er een fout gegenereerd.
Interne declaraties zijn handig voor het schrijven van modulaire code die opnieuw kan worden gebruikt door andere onderdelen van uw project, maar die later nog moeten worden gewijzigd zonder dat er andere projecten van afhankelijk zijn.

Een intern door de gebruiker gedefinieerd type, een bewerking of een functie kan eenvoudigweg worden gedeclareerd door `internal` toe te voegen aan het begin van de declaratie.
Bijvoorbeeld:

```qsharp
internal newtype PairOfQubits = (Qubit, Qubit);

internal operation PrepareEntangledPair(pair : PairOfQubits) : Unit 
is Adj + Ctl {
    let (q1, q2) = pair!;
    H(q2);
    CNOT(q2, q1);
}

internal function DotProduct(a : Double[], b : Double[]) : Double {
    ...
}
```

> [!WARNING]
> Intern door de gebruiker gedefinieerde typen kunnen alleen worden gebruikt in hand tekeningen of onderliggende typen als het overeenkomstige aanroep bare of door de gebruiker gedefinieerde type ook intern is.
> Als er bijvoorbeeld een door de gebruiker gedefinieerd type `InternalOptions` is gedeclareerd met het sleutel woord `internal`, resulteren de volgende declaraties in fouten:
>
> ```qsharp
> // Error: Can't use InternalOptions as an output type of a public function.
> function DefaultInternalOptions() : InternalOptions { ... }
>
> // Error: Can't use InternalOptions as an item in a public user-defined type.
> newtype ExtendedOptions = (Internal : InternalOptions);
> ```
