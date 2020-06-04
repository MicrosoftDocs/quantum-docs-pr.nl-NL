---
title: 'Bewerkingen en functies in Q #'
description: Bewerkingen en functies definiëren en aanroepen, evenals de gecontroleerde en adjoint bewerkingen.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: 9e924b973c4f22a59dd862df3f4f0d70278a1b4e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327795"
---
# <a name="operations-and-functions-in-q"></a>Bewerkingen en functies in Q #

## <a name="defining-new-operations"></a>Nieuwe bewerkingen definiëren

Bewerkingen zijn de kern van Q #.
Als ze zijn gedeclareerd, kunnen ze worden aangeroepen vanuit klassieke .NET-toepassingen, bijvoorbeeld met behulp van een Simulator of door andere bewerkingen binnen Q #.
Elke bewerking die is gedefinieerd in Q # kan vervolgens een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde intrinsieke bewerkingen die zijn gedefinieerd door de taal. De specifieke manier waarop deze intrinsieke bewerkingen worden gedefinieerd, is afhankelijk van de doel computer.
Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.

Elk Q #-bron bestand kan een wille keurig aantal bewerkingen definiëren.
Bewerkings namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met type-of functie namen.

Een bewerkings declaratie bestaat uit het tref woord `operation` , gevolgd door het symbool dat de naam van de bewerking is, een getypeerde id-tupel waarmee de argumenten voor de bewerking worden gedefinieerd, een dubbele punt `:` , een type aantekening waarmee het resultaat type van de bewerking wordt beschreven, optioneel een aantekening met de bewerkings kenmerken, een open accolade `{` , de hoofd tekst van de bewerkings `}`

Elke bewerking neemt een invoer, produceert een uitvoer en geeft de implementatie aan voor een of meer bewerkings-specials.
De mogelijke specials en hoe u deze kunt definiëren/aanroepen, worden verder uitgebreid beschreven.
Bekijk nu de volgende bewerking, waarmee alleen een standaard hoofd tekst wordt gedefinieerd en waarbij één Qubit als invoer wordt gebruikt. vervolgens wordt de ingebouwde <xref:microsoft.quantum.intrinsic.x> bewerking voor die invoer aangeroepen:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Het sleutel woord `operation` begint de definitie van de bewerking en wordt gevolgd door de naam; hier, `BitFlip` .
Vervolgens wordt het type van de invoer gedefinieerd als `Qubit` , samen met een naam `target` voor het verwijzen naar de invoer binnen de nieuwe bewerking.
Op dezelfde manier `Unit` wordt met de definitie aangegeven dat de uitvoer van de bewerking leeg is.
Dit wordt op dezelfde manier gebruikt als `void` in C# en andere verplichte talen en is gelijk aan `unit` in F # en andere functionele talen.

Bewerkingen kunnen ook interessante typen retour neren dan `Unit` .
De <xref:microsoft.quantum.intrinsic.m> bewerking retourneert bijvoorbeeld een uitvoer van het type `Result` , die aangeeft dat een meting is uitgevoerd. We kunnen de uitvoer van een bewerking door geven aan een andere bewerking of deze gebruiken met het `let` sleutel woord om een nieuwe variabele te definiëren.

Dit maakt het mogelijk om klassieke berekeningen aan te duiden die met Quantum bewerkingen op een laag niveau reageren, zoals bij de [code ring](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)van de functie:

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> Elke bewerking in Q # heeft precies één invoer en retourneert precies één uitvoer.
> Meerdere invoer en uitvoer worden vervolgens weer gegeven met behulp van *Tuples*, waarbij meerdere waarden worden verzameld in één waarde.
> We zeggen dat Q # een ' tuple-in ' tuple-out ' is.
> Dit concept `()` moet worden gelezen als de ' empty ' tuple, die van het type is `Unit` .


## <a name="controlled-and-adjoint-operations"></a>Gecontroleerde en adjoint bewerkingen

Als een bewerking een unitary-trans formatie implementeert, zoals het geval is voor veel bewerkingen in Q #, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt. Met een *adjoint* specialisatie van een bewerking wordt aangegeven hoe de ' inverse ' van de bewerking wordt uitgevoerd, terwijl een *beheerde* specialisatie aangeeft hoe een bewerking wordt uitgevoerd wanneer de toepassing wordt ingesteld op de status van een bepaalde Quantum register.

Adjoints van Quantum bewerkingen zijn cruciaal voor veel aspecten van Quantum Computing. Hieronder vindt u in de sectie [Conjugations](#conjugations) een dergelijke situatie die wordt besproken naast een handige Q #-programmeer techniek.

De gecontroleerde versie van een bewerking is een nieuwe bewerking waarbij de basis bewerking alleen effectief wordt toegepast als alle besturings elementen qubits een opgegeven status hebben.
Als het besturings element qubits zich in de superpositie bevindt, wordt de basis bewerking samenhangend toegepast op het juiste deel van de superpositie.
Daarom worden beheerde bewerkingen vaak gebruikt voor het genereren van Entanglement.

Natuurlijk kan ook een *beheerde adjoint* -specialisatie bestaan en de gecontroleerde toepassing van de adjoint van een bewerking opgeven.

> [!NOTE]
> Als $U $ de unitary-trans formatie is die door een bewerking wordt geïmplementeerd `U` , `Adjoint U` vertegenwoordigt de unitary-trans formatie $U ^ \dagger $, de complex geconjugeerde getransponeerde.
> Als er een bewerking wordt toegepast en vervolgens de adjoint naar een status, blijft de status ongewijzigd, zoals wordt geïllustreerd door $UU ^ \dagger = U ^ \dagger U = \id $, de identiteits matrix.
> De unitary-weer gave van een gecontroleerde bewerking is iets ingewik complexer, maar u kunt meer informatie vinden over de [concepten van Quantum Computing: meerdere qubits](xref:microsoft.quantum.concepts.multiple-qubits).

In de volgende sectie wordt beschreven hoe u deze verschillende specials aanroept in uw Q #-code.
Hieronder vindt u informatie over het definiëren van bewerkingen ter ondersteuning van deze activiteiten.

### <a name="calling-operation-specializations"></a>Bewerkings specials aanroepen

Een *functor* in Q # is een Factory die een nieuwe bewerking vanuit een andere bewerking definieert.
De twee standaard functors in Q # zijn `Adjoint` en `Controlled` .

Functors hebben toegang tot de implementatie van de basis bewerking bij het definiëren van de implementatie van de nieuwe bewerking.
Daarom kunnen functors complexere functies uitvoeren dan traditionele functies op een hoger niveau. Functors hebben geen weer gave in het Q #-type systeem. Het is dus niet mogelijk om deze aan een variabele te binden of als argumenten door te geven. 

Een functor wordt gebruikt door deze toe te passen op een bewerking en een nieuwe bewerking te retour neren.
De bewerking die het resultaat is van het Toep assen van de `Adjoint` functor op de `Y` bewerking, wordt bijvoorbeeld als volgt geschreven `Adjoint Y` .
De nieuwe bewerking kan vervolgens worden aangeroepen, zoals elke andere bewerking.
Voor een bewerking ter ondersteuning van de toepassing van de `Adjoint` en/of `Controlled` functors moet het retour type daarvan nood zakelijk zijn `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint`functor

`Adjoint Y(q1)`Op die manier wordt de adjoint functor toegepast op de `Y` bewerking om een nieuwe bewerking te genereren en wordt deze nieuwe bewerking toegepast op `q1` .
De nieuwe bewerking heeft dezelfde hand tekening en type als de basis bewerking `Y` .
Met name de nieuwe bewerking staat ook `Adjoint` toe en is alleen toegestaan als `Controlled` de basis bewerking is uitgevoerd.
De adjoint-functor is zijn eigen inverse; dat wil zeggen, `Adjoint Adjoint Op` is altijd hetzelfde als `Op` .

#### <a name="controlled-functor"></a>`Controlled`functor

Op dezelfde manier wordt `Controlled X(controls, target)` de beheerde functor toegepast op de `X` bewerking voor het genereren van een nieuwe bewerking en wordt die nieuwe bewerking toegepast op `controls` en `target` .

> [!NOTE]
> In Q # maken bewaakte versies altijd een matrix van besturings element qubits en de opgegeven status is altijd voor alle besturings elementen qubits in de status berekening ( `PauliZ` ) `One` , $ \ket {1} $.
> Het beheer op basis van andere Staten kan worden bereikt door de juiste unitary-bewerking toe te passen op de controle qubits vóór de gecontroleerde bewerking en vervolgens de inverse van de unitary-bewerking toe te passen na de gecontroleerde bewerking.
> Als u bijvoorbeeld een `X` bewerking toepast op een besturings element Qubit vóór en na een beheerde bewerking, wordt de bewerking voor het beheren van de `Zero` status ($ \ket {0} $) voor die Qubit uitgevoerd. het Toep assen van een `H` bewerking voor en na heeft tot gevolg `PauliX` `One` dat-1 eigenvalue van Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ in plaats van de `PauliZ` `One` status.

Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Controlled` functor.
De hand tekening van de nieuwe bewerking is gebaseerd op de hand tekening van de oorspronkelijke bewerking.
Het resultaat type is hetzelfde, maar het invoer type is een twee-tuple met een Qubit-matrix met de Qubit (s) die het eerste element bevat en de argumenten van de oorspronkelijke bewerking als het tweede element.
De nieuwe bewerking ondersteunt `Controlled` , en wordt alleen ondersteund als `Adjoint` de oorspronkelijke bewerking is uitgevoerd.

Als de oorspronkelijke bewerking slechts één argument heeft gevolgd, komt de singleton-tuple-equivalentie hier te staan.
Bijvoorbeeld, `Controlled X` is de beheerde versie van de `X` bewerking. 
`X`heeft type `(Qubit => Unit is Adj + Ctl)` , dus `Controlled X` heeft type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; vanwege Singleton-tuple-equivalentie is dit hetzelfde als `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Als de basis bewerking meerdere argumenten heeft, moet u de overeenkomstige argumenten van de gecontroleerde versie van de bewerking tussen haakjes plaatsen om ze te converteren naar een tuple.
Bijvoorbeeld, `Controlled Rz` is de beheerde versie van de `Rz` bewerking. 
`Rz`heeft type `((Double, Qubit) => Unit is Adj + Ctl)` , dus `Controlled Rz` heeft type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Dit is dus `Controlled Rz(controls, (0.1, target))` een geldige aanroep van `Controlled Rz` (Let op de haakjes rond `0.1, target` ).

Een ander voor beeld `CNOT(control, target)` kan worden geïmplementeerd als `Controlled X([control], target)` . Als een doel moet worden beheerd door 2 Control qubits (CCNOT), kunnen we de `Controlled X([control1, control2], target)` instructie gebruiken.

#### `Controlled Adjoint` 

Het `Controlled` en `Adjoint` functors werk, dus er is geen verschil tussen het Toep assen van `Controlled Adjoint Op` of `Adjoint Controlled Op` .


## <a name="defining-controlled-and-adjoint-implementations"></a>Beheerde en adjoint-implementaties definiëren

In de eerste voor beelden van bewerkings declaraties zijn de bewerkingen `BitFlip` en `DecodeSuperdense` zijn gedefinieerd met hand tekeningen `(Qubit => Unit)` en `((Qubit, Qubit) => (Result, Result))` respectievelijk.
Net als bij `DecodeSuperdense` metingen, is het geen unitary-bewerking en zijn er geen beheerde niet-adjointe specials mogelijk (roep de gerelateerde vereiste in die een dergelijke bewerking retourneert `Unit` ).
Als `BitFlip` simpelweg de unitary <xref:microsoft.quantum.intrinsic.x> -bewerking uitvoert, kunnen we deze echter wel met beide specials hebben gedefinieerd.

Hier wordt beschreven hoe u het bestaan van specials in uw Q #-bewerkings declaraties opneemt, zodat ze kunnen worden aangeroepen in combi natie met de `Adjoint` en/of `Controlled` functors.
[Hieronder](#circumstances-for-validly-defining-specializations)worden enkele situaties beschreven waarin het geldig is of niet geldig is voor het declareren van bepaalde specials.

Met bewerkings kenmerken wordt gedefinieerd welke soorten functors kunnen worden toegepast op de gedeclareerde bewerking en welk effect ze hebben. Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking, met name door een aantekening met de bewerkings kenmerken: ofwel `is Adj` , `is Ctl` of `is Adj + Ctl` .
De daad werkelijke implementatie van elke specialisatie kan *impliciet* of *expliciet* worden gedefinieerd.

### <a name="implicitly-specifying-implementations"></a>Impliciete implementaties opgeven

In dit geval bestaat de hoofd tekst van de bewerkings declaratie uit uitsluitend de standaard implementatie. Bijvoorbeeld:

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
Hier wordt de overeenkomstige implementatie voor elke impliciet gedeclareerde specialisatie automatisch gegenereerd door de compiler om te worden uitgevoerd als de `Adjoint` of `Controlled` functors wordt gebruikt.

Daarom zou een aanroep van `Adjoint PrepareEntangledPair` zouden leiden tot het compileren van de adjoint van `CNOT` en vervolgens de adjoint van `H` .
Deze afzonderlijke bewerkingen zijn beide Self-adjoint, dus de resulterende `Adjoint PrepareEntangledPair` bewerking zou gewoon bestaan `CNOT(here, there)` en vervolgens worden toegepast `H(here)` .
Daarom kunnen we dit gebruiken om het `DecodeSuperdense` bovenstaande voor beeld sneller te schrijven, met behulp van de adjoint van `PrepareEntangledPair` om de Entangled-status terug te zetten in een unentangled paar qubits:

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

De aantekening met de bewerkings kenmerken in de declaratie is handig om ervoor te zorgen dat de compiler automatisch andere specials wordt gegenereerd op basis van de standaard implementatie. 

Er zijn een aantal belang rijke beperkingen waarmee u rekening moet houden bij het ontwerpen van bewerkingen voor gebruik met functors.
De meeste van de voor delen van een bewerking die de uitvoer waarde van een andere bewerking gebruikt, *kan niet* automatisch worden gegenereerd door de compiler, omdat het niet eenduidig is hoe u de instructies in een dergelijke bewerking opnieuw ordent om hetzelfde effect te verkrijgen.

Daarom is het vaak handig om de verschillende implementaties expliciet op te geven.

### <a name="explicitly-specifying-implementations"></a>Expliciet opgeven van implementaties

Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven. Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte instructie voor het *genereren* of een door de gebruiker gedefinieerde implementatie.
Hier bieden we het volledige aanbod van mogelijkheden, met voor beelden hieronder.


#### <a name="explicit-specialization-declarations"></a>Expliciete specialisatie declaraties

Q #-bewerkingen kunnen de volgende expliciete specialisatie declaraties bevatten:

- De `body` specialisatie specificeert de implementatie van de bewerking waarvoor geen functors is toegepast.
- De `adjoint` specialisatie specificeert de implementatie van de bewerking waarop de `Adjoint` functor is toegepast.
- De `controlled` specialisatie specificeert de implementatie van de bewerking waarop de `Controlled` functor is toegepast.
- De `controlled adjoint` specialisatie specificeert de implementatie van de bewerking waarbij de `Adjoint` en `Controlled` functors zijn toegepast.
  Deze specialisatie kan ook worden genoemd `adjoint controlled` , omdat de twee functors werkend zijn.


Een specialisatie bewerking bestaat uit het specialisatie label (bijvoorbeeld `body` of `adjoint` , enzovoort), gevolgd door een van de volgende opties:

- Een expliciete declaratie zoals hieronder wordt beschreven.
- Een *instructie* die de compiler vertelt *hoe* de specialisatie moet worden gegenereerd, een van de volgende opties:
  - `intrinsic`. Dit geeft aan dat de specialisatie wordt verschaft door de doel computer.
  - `distribute`, die kunnen worden gebruikt met de `controlled` en `controlled adjoint` specials.
    Bij gebruik met `controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door toe `Controlled` te passen op alle bewerkingen in de `body` .
    Bij gebruik met `controlled adjoint` geeft dit aan dat de compiler de specialisatie moet berekenen door `Controlled` alle bewerkingen in de specialisatie toe te passen `adjoint` .
  - `invert`Dit geeft aan dat de compiler de `adjoint` specialisatie moet berekenen door de `body` , dat wil zeggen de volg orde van de bewerkingen en het Toep assen van de adjoint op elke waarde.
    Bij gebruik met `adjoint controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door de specialisatie te omkeren `controlled` .
  - `self`om aan te geven dat de adjoint specialize hetzelfde is als de `body` specialisatie.
    Dit is juridisch voor de `adjoint` en `adjoint controlled` specials.
    Voor `adjoint controlled` `self` betekent dat de `adjoint controlled` specialisatie hetzelfde is als de `controlled` specialisatie.
  - `auto`om aan te geven dat de compiler een geschikte richt lijn moet selecteren om toe te passen.
    `auto`kan niet worden gebruikt voor de `body` specialisatie.

De richt lijnen en `auto` alle vereisen een sluitende punt komma `;` .
De `auto` instructie wordt omgezet in de volgende generatie-instructie als een expliciete declaratie van de `body` wordt gegeven:

- De `adjoint` specialisatie wordt gegenereerd volgens de instructie `invert` .
- De `controlled` specialisatie wordt gegenereerd volgens de instructie `distribute` .
- De `adjoint controlled` specialisatie wordt gegenereerd volgens de richt lijn `invert` als een expliciete declaratie voor `controlled` is opgegeven, maar niet een voor `adjoint` , en `distribute` anders.

> [!TIP]   
> Als een bewerking zelf adjoint is, geeft u expliciet de adjoint of de bewaakte adjoint-specialisatie op via de generatie-instructie `self` zodat de compiler gebruik van die informatie kan maken voor optimaliserings doeleinden.

Een specialisatie declaratie met een door de gebruiker gedefinieerde implementatie bestaat uit een argument tuple gevolgd door een instructie blok met de Q #-code die de specialisatie implementeert.
In de argumenten lijst `...` wordt gebruikt om de argumenten weer te geven die zijn gedeclareerd voor de bewerking als geheel.
Voor `body` en `adjoint` , de lijst met argumenten moet altijd zijn `(...)` : voor `controlled` en `adjoint controlled` , de lijst met argumenten moet een symbool zijn dat de matrix van besturings element qubits, gevolgd door `...` , tussen haakjes (bijvoorbeeld) `(controls,...)` .

### <a name="examples"></a>Voorbeelden

Een bewerkings declaratie kan zo eenvoudig zijn als het volgende, wat de primitieve Pauli X-bewerking definieert:

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
Houd er rekening mee dat de adjoint van de Pauli X-bewerking is gedefinieerd met de instructie, `self` omdat de `X` eigen inverse van de definitie.

De bovenstaande code `PrepareEntangledPair` is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
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

#### <a name="user-defined-specialization-implementation"></a>Door de gebruiker gedefinieerde implementatie van specialisatie

Als de compiler de implementatie voor een bepaalde specialisatie niet automatisch kan genereren of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.

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
In het bovenstaande voor beeld `adjoint invert;` geeft aan dat de adjoint-specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie te omkeren.

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

### <a name="circumstances-for-validly-defining-specializations"></a>Omstandigheden voor het op geldige wijze definiëren van specials

#### <a name="operation-declarations-with-adjointcontrolled"></a>Bewerkings declaraties met adjoint/beheerd

Het is wettelijk om een bewerking zonder adjoint of beheerde versies op te geven. Meting bewerkingen hebben bijvoorbeeld geen, omdat ze niet omkeerbaar of niet kunnen worden bestuurd.

Een bewerking ondersteunt de `Adjoint` en/of `Controlled` functors als de bijbehorende declaratie een impliciete of expliciete declaratie van de respectieve specials bevat.

Een expliciet aangegeven adjoint/beheerde specialisatie impliceert dat er een adjoint/beheerde specialisatie bestaat. 

Voor een bewerking waarvan de hoofd tekst herhalen-until-success-lussen, set-instructies, metingen, retour overzichten of aanroepen naar andere bewerkingen die de functor niet ondersteunen `Adjoint` , het automatisch genereren van een adjoint-specialisatie volgens de `invert` or- `auto` instructie is niet mogelijk.

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen ondersteuning bieden voor de `Controlled` functor, wordt het automatisch genereren van een gecontroleerde specialisatie volgens de `distribute` or- `auto` instructie niet mogelijk.

#### <a name="controlled-adjoint"></a>Beheerde adjoint

De gecontroleerde adjoint-versie van een bewerking geeft aan hoe een Quantum versie van de adjoint van de bewerking wordt geïmplementeerd.
Het is niet toegestaan een bewerking op te geven zonder beheerde adjoint-versie. meting bewerkingen hebben bijvoorbeeld geen beheerde adjoint-versie omdat ze niet kunnen worden ingesteld of omkeerbaar.

Een beheerde adjoint-specialisatie voor een bewerking moet bestaan als en alleen als zowel een adjoint als een beheerde specialisatie bestaan. In dat geval wordt het bestaan van de beheerde adjoint-specialisatie afgeleid en wordt er een geschikte specialisatie gegenereerd door de compiler als er expliciet geen implementatie is gedefinieerd. 

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen beheerde adjoint-versie hebben, wordt het automatisch genereren van een adjoint specialisatie na de `invert` `distribute` of- `auto` instructie niet mogelijk.


### <a name="type-compatibility"></a>Type compatibiliteit

Een bewerking met aanvullende functors-ondersteuning kan worden gebruikt op een wille keurige locatie met minder functors, maar dezelfde hand tekening wordt verwacht.
Een bewerking van het type kan bijvoorbeeld `(Qubit => Unit is Adj)` worden gebruikt overal een bewerking van het type `(Qubit => Unit)` wordt verwacht.

Q # is *covariantie* ten opzichte van aanroep bare retour typen: een aanroepable die een type retourneert `'A` , is compatibel met een aanroepbaar met hetzelfde invoer type en een resultaat type dat `'A` compatibel is met.

Q # is *contra variant* met betrekking tot invoer typen: een aanroepable die een type `'A` als invoer vereist, is compatibel met een aanroepbaar met hetzelfde resultaat type en een invoer type dat compatibel is met `'A` .

Dat wil zeggen, op basis van de volgende definities:

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

de volgende voor waarden zijn waar:

- De functie `ConjugateInvertWith` kan worden aangeroepen met een `inner` argument van ofwel `Invert` of `ApplyUnitary` .
- De functie `ConjugateUnitaryWith` kan worden aangeroepen met een `inner` argument van `ApplyUnitary` , maar niet `Invert` .
- Er kan een waarde van het type `(Qubit[] => Unit is Adj + Ctl)` worden geretourneerd van `ConjugateInvertWith` .

> [!IMPORTANT]
> Q # 0,3 heeft een aanzienlijk verschil in het gedrag van door de gebruiker gedefinieerde typen geïntroduceerd.

Door de gebruiker gedefinieerde typen worden behandeld als een ingepakte versie van het onderliggende type, in plaats van als subtype.
Dit betekent dat een waarde van een door de gebruiker gedefinieerd type niet kan worden gebruikt als een waarde van het onderliggende type wordt verwacht.


### <a name="conjugations"></a>Conjugations

In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn. Dit kan worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven. Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

Vanaf onze 0,9-release ondersteunen we een conjugation-instructie die de bovenstaande trans formatie implementeert. Met deze instructie kan de bewerking `ApplyWith` op de volgende manier worden geïmplementeerd:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Een dergelijke conjugation-instructie is natuurlijk veel handiger als de buitenste en de binnenste trans formatie niet onmiddellijk beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies. 

De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid.
Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok. 


## <a name="defining-new-functions"></a>Nieuwe functies definiëren

Functions zijn louter deterministische, klassieke routines in Q #, die verschillend zijn van bewerkingen in dat ze geen invloed mogen hebben op de berekening van een uitvoer waarde.
Met name functies kunnen geen bewerkingen aanroepen; actie ondernemen, toewijzen of lenen qubits; voor beelden van wille keurige getallen; of op andere wijze, afhankelijk van de invoer waarde voor een functie.
Als gevolg hiervan zijn Q #-functies *puur*, in dat ze altijd dezelfde invoer waarden toewijzen aan dezelfde uitvoer waarden.
Hiermee kan de Q #-compiler veilig de volg orde wijzigen van hoe en wanneer-functies worden aangeroepen bij het genereren van bewerkings-specials.

Elk Q #-bron bestand kan een wille keurig aantal functies definiëren.
Functie namen moeten uniek zijn binnen een naam ruimte en kunnen een conflict veroorzaken met bewerkingen of type namen.

Het definiëren van een functie werkt op dezelfde manier als het definiëren van een bewerking, behalve dat er geen adjoint of beheerde Specials kunnen worden gedefinieerd voor een functie.
Bijvoorbeeld:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

of 

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

### <a name="classical-logic-in-functions--good"></a>Klassieke logica in functions = = goed

Wanneer het mogelijk is om dit te doen, is het handig om klassieke logica te schrijven in termen van functies in plaats van bewerkingen, zodat deze gemakkelijk vanuit bewerkingen kan worden gebruikt.
Als we bijvoorbeeld de bovenstaande declaratie hebben geschreven `Square` als een *bewerking*, zou de compiler niet kunnen garanderen dat het aanroepen van deze met dezelfde invoer consequent dezelfde uitvoer produceert.

Als u het verschil tussen functies en bewerkingen wilt onderstrepen, moet u rekening houden met het probleem van klassieke steek proeven voor een wille keurig getal in een Q #-bewerking:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Elke keer dat `U` wordt aangeroepen, heeft het een andere actie `target` .
In het bijzonder kan de compiler niet garanderen dat als we een `adjoint auto` specialisatie-declaratie aan hebben toegevoegd `U` , vervolgens `U(target); Adjoint U(target);` fungeren als identiteit (dat wil zeggen, als niet op).
Dit schendt de definitie van de adjoint die we hebben gezien in [vectoren en matrices](xref:microsoft.quantum.concepts.vectors), waardoor het automatisch genereren van een adjoint-specialisatie in een bewerking waarbij de bewerking werd aangeroepen, <xref:microsoft.quantum.math.randomreal> de door de compiler geboden garanties zou verstoren; <xref:microsoft.quantum.math.randomreal> is een bewerking waarvoor geen adjoint of gecontroleerde versie bestaat.

Aan de andere kant, waardoor functie aanroepen zoals `Square` veilig kunnen worden uitgevoerd, kan worden gegarandeerd dat de compiler alleen de invoer moet behouden om de `Square` uitvoer stabiel te houden.
Door zo veel mogelijk klassieke logica in functies te isoleren, is het eenvoudig om die logica in andere functies en bewerkingen hetzelfde te hergebruiken.


## <a name="generic-type-parameterized-callables"></a>Algemene Callables (type parameters)

Veel functies en bewerkingen die u mogelijk wilt definiëren, zijn niet echt afhankelijk van de typen invoer, maar u kunt de typen echter alleen impliciet gebruiken via een andere functie of bewerking.
Stel dat het *kaart* concept gebruikelijk is in veel functionele talen. op basis van een functie $f (x) $ en een verzameling waarden $ \{ x_1, x_2, \dots, x_n \} $, kaart retourneert een nieuwe verzameling $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.
Om dit in Q # te implementeren, kunnen we profiteren van die functies de eerste klasse.
We gaan een snel voor beeld van `Map` maken, met ★ als tijdelijke aanduiding, terwijl we weten wat voor typen we nodig hebben.

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
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
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

In principe zou we een versie van kunnen schrijven `Map` voor elk paar typen dat we tegen komen, maar dit heeft een aantal problemen.
Als we bijvoorbeeld een bug in hebben gevonden `Map` , moeten we ervoor zorgen dat de oplossing op uniforme wijze wordt toegepast in alle versies van `Map` .
Als we een nieuwe tuple of UDT bouwen, moeten we nu ook een nieuwe `Map` combi natie maken met het nieuwe type.
Hoewel dit kan worden beperkt door een klein aantal dergelijke functies, omdat we meer en meer functies van hetzelfde formulier verzamelen, worden `Map` de kosten van het introduceren van nieuwe typen onredelijk groot in een redelijk korte volg orde.

Veel van deze problemen kunnen er echter toe leiden dat we de compiler niet hebben gezien de informatie die nodig is om te bepalen hoe de verschillende versies van `Map` zijn gerelateerd.
Effectief moeten we de compiler behandelen `Map` als een soort wiskundige functie van q #- *typen* naar q #-functies.

Dit principe wordt formeel door het toestaan van functies en bewerkingen om *type parameters*te hebben, evenals de normale tuple-para meters.
In de bovenstaande voor beelden willen we nadenken over `Map` de typen para meters `Int, Pauli` in het eerste geval en `Double, String` in het tweede geval.
In het algemeen kunnen deze type parameters vervolgens worden gebruikt alsof het normale typen zijn: we gebruiken waarden van het type para meters om matrices en Tuples te maken, functies en bewerkingen aan te roepen en toe te wijzen aan gewone of onveranderlijke variabelen.

> [!NOTE]
> Het meest extreme geval van indirecte afhankelijkheid is die van qubits, waarbij een Q #-programma niet rechtstreeks kan vertrouwen op de structuur van het `Qubit` type, maar **moet** dergelijke typen door geven aan andere bewerkingen en functies.

Als u terugkeert naar het bovenstaande voor beeld, kunnen we zien dat we `Map` type-para meters moeten hebben, een voor de invoer tot `fn` en met één om de uitvoer van weer te geven `fn` .
In Q # wordt dit geschreven door punt haken (dat wil zeggen `<>` , niet brakets $ \braket $!) toe te voegen {} na de naam van een functie of bewerking in de declaratie en door elke type parameter te vermelden.
De naam van elke type parameter moet beginnen met een streepje `'` , wat aangeeft dat het een type parameter is en niet een normaal type (ook wel een *concreet* type genoemd).
Voor kunnen `Map` we het volgende schrijven:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Houd er rekening mee dat de definitie van een `Map<'Input, 'Output>` uitermate gelijkenis lijkt met de versies die we eerder hebben afgeschreven.
Het enige verschil is dat we het Compileer programma expliciet hebben geïnformeerd dat `Map` niet rechtstreeks afhankelijk is van wat en dat wel `'Input` `'Output` , maar wel voor twee typen, met behulp van deze indirect via `fn` .
Zodra we `Map<'Input, 'Output>` op deze manier zijn gedefinieerd, kunnen we deze aanroepen alsof het een gewone functie was:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Het schrijven van algemene functies en bewerkingen is een plek waar ' tuple-in ' tuple-out ' een zeer handige manier is om te denken over Q #-functies en-bewerkingen.
> Omdat voor elke functie precies één invoer wordt gebruikt en er precies één uitvoer wordt geretourneerd, komt een invoer van het type `'T -> 'U` overeen met *elke* Q #-functie.
> Elke bewerking kan ook worden door gegeven aan een invoer van het type `'T => 'U` .

Als tweede voor beeld moet u de uitdaging van het schrijven van een functie die de samen stelling van twee andere functies retourneert, overwegen:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier moeten we precies opgeven wat `A` , `B` en `C` zijn, waardoor het hulp programma van onze nieuwe functie ernstig wordt beperkt `Compose` .
Daarna `Compose` is alleen afhankelijk van `A` , `B` en `C` *via* `innerFn` en `outerFn` .
Als alternatief kunnen we type parameters toevoegen aan `Compose` die aangeven dat het werkt voor *elk* `A` , `B` en, `C` zolang deze para meters overeenkomen met de verwachte `innerFn` en `outerFn` :

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


## <a name="callables-as-first-class-values"></a>Callables als waarden voor de eerste klasse

Een van de essentiële technieken voor het opwegen van de controle stroom en klassieke logica met behulp van functies in plaats van bewerkingen is het gebruik van die bewerkingen en functies in Q # zijn de *eerste klasse*.
Dat wil zeggen dat ze elke waarde in de taal in hun eigen recht zijn.
Het volgende is bijvoorbeeld een zeer geldige Q #-code, als een beetje indirect:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

De waarde van de variabele `ourH` in het bovenstaande fragment is vervolgens de bewerking <xref:microsoft.quantum.intrinsic.h> , zodat we deze waarde kunnen aanroepen, zoals elke andere bewerking.
Hierdoor kunnen we bewerkingen schrijven die bewerkingen als onderdeel van hun invoer doen, waardoor de controle stroom concepten met een hogere volg orde kunnen worden uitgevoerd.
We kunnen bijvoorbeeld Voorst Ellen om een bewerking te ' Square ' door deze twee keer op dezelfde doel-Qubit toe te passen.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Bewerkingen van een functie retour neren

We zijn van belang dat we ook bewerkingen kunnen retour neren als onderdeel van de uitvoer, zodat we bepaalde soorten klassieke voorwaardelijke logica kunnen isoleren als een klassieke functie waarmee een beschrijving van een Quantum programma wordt geretourneerd in de vorm van een bewerking.
Als eenvoudig voor beeld kunt u het voor beeld van teleportie overwegen, waarbij de partij die een twee-bits klassiek bericht ontvangt, het bericht moet gebruiken om hun Qubit te decoderen naar de juiste teleportal-status.
We kunnen dit schrijven in termen van een functie die deze twee klassieke bits accepteert en de juiste decodeer bewerking retourneert.

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

Deze nieuwe functie is inderdaad een functie, in dat geval als we deze aanroepen met dezelfde waarden van `hereBit` en `thereBit` , zullen we altijd dezelfde bewerking ophalen.
Het is dus mogelijk dat de decoder veilig kan worden uitgevoerd binnen bewerkingen zonder dat dit de reden hoeft te zijn van de manier waarop de decodeer logica communiceert met de definities van de verschillende bewerkings-specials.
Dat wil zeggen dat we de klassieke logica binnen een functie hebben geïsoleerd, zodat de compiler kan worden gevolgd met impunity, zolang de invoer wordt bewaard.


## <a name="partial-application"></a>Gedeeltelijke toepassing

We kunnen aanzienlijk meer doen met functies die bewerkingen retour neren met behulp van *gedeeltelijke toepassing*, waarbij we een of meer delen van de invoer kunnen bieden aan een functie of bewerking zonder dat deze daad werkelijk wordt aangeroepen. `ApplyTwice`Als u bijvoorbeeld het bovenstaande voor beeld aanroept, kunt u aangeven dat we niet meteen willen opgeven, op welke Qubit de invoer bewerking moet worden toegepast:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In dit geval bevat de lokale variabele `twiceOp` de gedeeltelijk toegepaste bewerking `ApplyTwice(op, _)` , waarbij delen van de invoer die nog niet zijn opgegeven, worden aangegeven door `_` .
Wanneer we de volgende regel daad werkelijk aanroepen `twiceOp` , geven we de invoer door aan de gedeeltelijk toegepaste bewerking van alle resterende delen van de invoer voor de oorspronkelijke bewerking.
Het bovenstaande code fragment is dus in feite identiek aan het `ApplyTwice(op, target)` rechtstreeks aanroepen van, opslaan voor dat we een nieuwe lokale variabele hebben geïntroduceerd waarmee we de oproep kunnen vertragen tijdens het leveren van bepaalde onderdelen van de invoer.

Omdat een bewerking die gedeeltelijk is toegepast, niet daad werkelijk wordt aangeroepen totdat de volledige invoer is opgegeven, kunnen we bewerkingen gedeeltelijk Toep assen, zelfs binnen functies.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

In principe is de klassieke logica binnen `SquareOperation` mogelijk veel meer betrokken, maar is deze nog steeds geïsoleerd van de rest van een bewerking door de garanties dat de compiler over functies kan bieden.
Deze benadering wordt gebruikt in de standaard bibliotheek van Q # voor het uitdrukken van de klassieke controle stroom op een manier die eenvoudig kan worden gebruikt binnen Quantum Program ma's.


## <a name="recursion"></a>Recursie

Q # callables mogen direct of indirect recursief zijn.
Dat wil zeggen dat een bewerking of functie zichzelf kan aanroepen, of een andere aanroep kan aanroepen die direct of indirect de aanroep bare bewerking aanroept.

Er zijn twee belang rijke opmerkingen over het gebruik van recursie, echter:

- Het gebruik van recursie in bewerkingen heeft waarschijnlijk een conflict met bepaalde optimalisaties.
  Dit kan een aanzienlijke invloed hebben op de uitvoerings tijd van de algoritme.
- Bij het uitvoeren van een echt Quantum apparaat kan de stack-ruimte beperkt zijn en kan een grondige recursie leiden tot een runtime-fout.
  Met name de Q #-compiler en runtime identificeren en optimaliseren de staart recursie niet.

## <a name="next-steps"></a>Volgende stappen

Meer informatie over [variabelen](xref:microsoft.quantum.guide.variables) in Q #.