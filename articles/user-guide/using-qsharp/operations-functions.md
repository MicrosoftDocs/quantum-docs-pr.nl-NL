---
title: Bewerkingen en functies inQ#
description: Bewerkingen en functies definiëren en aanroepen, evenals de gecontroleerde en adjoint bewerkingen.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 76437c83df894fa86409e680f961d97e267c6869
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867876"
---
# <a name="operations-and-functions-in-no-locq"></a>Bewerkingen en functies inQ#

## <a name="defining-new-operations"></a>Nieuwe bewerkingen definiëren

Bewerkingen zijn de kern van Q# .
Als ze eenmaal zijn gedeclareerd, kunnen ze worden aangeroepen vanuit klassieke .NET-toepassingen, bijvoorbeeld door gebruik te maken van een Simulator of door andere bewerkingen binnen Q# .
Elke bewerking die in Q# wordt gedefinieerd in, kan een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde intrinsieke bewerkingen die door de taal worden gedefinieerd. De specifieke manier waarop Q# deze intrinsieke bewerkingen worden gedefinieerd, is afhankelijk van de doel computer.
Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.

Elk Q# bron bestand kan elk wille keurig aantal bewerkingen definiëren.
Bewerkings namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met type-of functie namen.

Een bewerkings declaratie bestaat uit het tref woord `operation` , gevolgd door het symbool dat de naam van de bewerking is, een getypeerde id-tupel waarmee de argumenten voor de bewerking worden gedefinieerd, een dubbele punt `:` , een type aantekening waarmee het resultaat type van de bewerking wordt beschreven, optioneel een aantekening met de bewerkings kenmerken, een open accolade en de hoofd tekst van de bewerkings `{ }`

Elke bewerking neemt een invoer, produceert een uitvoer en geeft de implementatie aan voor een of meer bewerkings-specials.
De mogelijke specials en hoe u deze kunt definiëren en aanroepen, worden beschreven in de verschillende gedeelten van dit artikel.
Bekijk nu de volgende bewerking, waarmee alleen een standaard hoofd tekst wordt gedefinieerd en waarbij één Qubit als invoer wordt gebruikt. vervolgens wordt de ingebouwde <xref:microsoft.quantum.intrinsic.x> bewerking voor die invoer aangeroepen:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Het sleutel woord `operation` begint de bewerkings definitie, gevolgd door de naam; hier, `BitFlip` .
Vervolgens wordt het type invoer gedefinieerd ( `Qubit` ), samen met een naam, `target` voor het verwijzen naar de invoer binnen de nieuwe bewerking.
Hiermee wordt ten slotte `Unit` gedefinieerd dat de uitvoer van de bewerking leeg is.
`Unit`wordt op dezelfde manier gebruikt als `void` in C# en andere dwingende talen en is gelijk aan `unit` in F # en andere functionele talen.

Bewerkingen kunnen ook interessante typen retour neren dan `Unit` .
De <xref:microsoft.quantum.intrinsic.m> bewerking retourneert bijvoorbeeld een uitvoer van het type `Result` , die aangeeft dat een meting is uitgevoerd.  U kunt de bewerking door geven aan een andere bewerking of deze gebruiken met het `let` sleutel woord om een nieuwe variabele te definiëren.

Deze aanpak maakt het mogelijk om klassieke berekeningen te geven die met Quantum bewerkingen op een laag niveau reageren, zoals in de [code ring van de superdichte](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)snelheid:

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
> Elke bewerking in Q# heeft precies één invoer en retourneert precies één uitvoer.
> Meerdere invoer en uitvoer worden weer gegeven met behulp van *Tuples*, waarmee meerdere waarden worden verzameld in één waarde.
> In dit opzicht Q# is de taal ' tuple-in-tuple '.
> In dit concept moet een reeks lege haakjes `()` worden gelezen als de ' lege ' tuple, die het type heeft `Unit` .

## <a name="controlled-and-adjoint-operations"></a>Gecontroleerde en adjoint bewerkingen

Als een bewerking een unitary-trans formatie implementeert, zoals het geval is voor veel bewerkingen in Q# , is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt. Met een *adjoint* specialisatie van een bewerking wordt aangegeven hoe de ' inverse ' van de bewerking wordt uitgevoerd, terwijl een *beheerde* specialisatie aangeeft hoe een bewerking wordt uitgevoerd wanneer de toepassing wordt ingesteld op de status van een bepaalde Quantum register.

Adjoints van Quantum bewerkingen zijn cruciaal voor veel aspecten van Quantum Computing. Q#Zie [Conjugations](#conjugations) in dit artikel voor een voor beeld van een dergelijke situatie die wordt besproken naast een handige programmeer techniek. 

De gecontroleerde versie van een bewerking is een nieuwe bewerking waarbij de basis bewerking alleen effectief wordt toegepast als alle besturings elementen qubits een opgegeven status hebben.
Als het besturings element qubits zich in de superpositie bevindt, wordt de basis bewerking samenhangend toegepast op het juiste deel van de superpositie.
Daarom worden beheerde bewerkingen vaak gebruikt voor het genereren van Entanglement.

Natuurlijk kan ook een *beheerde adjoint* -specialisatie bestaan en de gecontroleerde toepassing van de adjoint van een bewerking opgeven.

> [!NOTE]
> Als $U $ de unitary-trans formatie is die door een bewerking wordt geïmplementeerd `U` , `Adjoint U` vertegenwoordigt de unitary-trans formatie $U ^ \dagger $, de complex geconjugeerde getransponeerde.
> Als er een bewerking wordt toegepast en vervolgens de adjoint naar een status, blijft de status ongewijzigd, zoals wordt geïllustreerd door $UU ^ \dagger = U ^ \dagger U = \id $, de identiteits matrix.
> De unitary-weer gave van een gecontroleerde bewerking is iets ingewik complexer, maar u kunt meer informatie vinden over de [concepten van Quantum Computing: meerdere qubits](xref:microsoft.quantum.concepts.multiple-qubits).

In de volgende sectie wordt beschreven hoe u deze verschillende specials in uw code aanroept Q# en hoe u bewerkingen definieert om ze te ondersteunen.

### <a name="calling-operation-specializations"></a>Bewerkings specials aanroepen

Een *functor* in Q# is een Factory die een nieuwe bewerking vanuit een andere bewerking definieert.
De twee standaard functors in Q# zijn `Adjoint` en `Controlled` .

Functors hebben toegang tot de implementatie van de basis bewerking bij het definiëren van de implementatie van de nieuwe bewerking.
Daarom kunnen functors complexere functies uitvoeren dan traditionele functies op een hoger niveau. Functors hebben geen weer gave in het Q# type systeem. Het is dus niet mogelijk om deze aan een variabele te binden of als argumenten door te geven. 

Gebruik een functor door het toe te passen op een bewerking, waardoor een nieuwe bewerking wordt geretourneerd.
`Adjoint`Als u bijvoorbeeld de functor toepast op de `Y` bewerking, wordt de nieuwe bewerking geretourneerd `Adjoint Y` . U kunt de nieuwe bewerking aanroepen, zoals elke andere bewerking.
Voor een bewerking die de toepassing van de `Adjoint` of `Controlled` functors ondersteunt, moet het retour type daarvan nood zakelijk zijn `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint`functor

`Adjoint Y(q1)`Op die manier wordt de `Adjoint` functor toegepast op de `Y` bewerking om een nieuwe bewerking te genereren en wordt die nieuwe bewerking toegepast op `q1` .
De nieuwe bewerking heeft dezelfde hand tekening en type als de basis bewerking `Y` .
In het bijzonder ondersteunt de nieuwe bewerking ook `Adjoint` `Controlled` als en alleen als de basis bewerking is gelukt.
De `Adjoint` functor is een eigen inverse; dat wil zeggen, `Adjoint Adjoint Op` is altijd hetzelfde als `Op` .

#### <a name="controlled-functor"></a>`Controlled`functor

Op dezelfde manier wordt `Controlled X(controls, target)` de `Controlled` functor toegepast op de `X` bewerking om een nieuwe bewerking te genereren en wordt die nieuwe bewerking toegepast op `controls` en `target` .

> [!NOTE]
> In worden Q# door gereguleerde versies altijd een matrix van besturings element qubits, en is de besturing altijd gebaseerd op alle besturings elementen qubits in de status berekenen ( `PauliZ` ) `One` , $ \ket {1} $.
> Het beheren op basis van andere statussen wordt bereikt door de juiste unitary-bewerking toe te passen op de controle qubits vóór de gecontroleerde bewerking en vervolgens de inverse van de unitary-bewerking toe te passen na de gecontroleerde bewerking.
> Als u bijvoorbeeld een `X` bewerking toepast op een besturings element Qubit vóór en na een beheerde bewerking, wordt de bewerking voor het beheren van de `Zero` status ($ \ket {0} $) voor die Qubit uitgevoerd; het Toep assen van een `H` bewerking voor en na de besturings elementen van de `PauliX` `One` status, die-1 eigenvalue van Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ in plaats van de `PauliZ` `One` status

Op basis van een bewerkings expressie kunt u een nieuwe bewerkings expressie maken met behulp van de `Controlled` functor.
De hand tekening van de nieuwe bewerking is gebaseerd op de hand tekening van de oorspronkelijke bewerking.
Het resultaat type is hetzelfde, maar het invoer type is een twee-tuple met een Qubit-matrix met de Qubit (s) die het eerste element bevat en de argumenten van de oorspronkelijke bewerking als het tweede element.
De nieuwe bewerking ondersteunt `Controlled` , en wordt alleen ondersteund als `Adjoint` de oorspronkelijke bewerking is uitgevoerd.

Als de oorspronkelijke bewerking slechts één argument heeft, wordt er hier een [Singleton-tuple-equivalentie](xref:microsoft.quantum.guide.types) weer gegeven.
Bijvoorbeeld, `Controlled X` is de beheerde versie van de `X` bewerking. 
`X`heeft type `(Qubit => Unit is Adj + Ctl)` , dus `Controlled X` heeft type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; vanwege Singleton-tuple-equivalentie is dit hetzelfde als `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Als de basis bewerking meerdere argumenten heeft, moet u de overeenkomstige argumenten van de gecontroleerde versie van de bewerking tussen haakjes plaatsen om ze te converteren naar een tuple.
Bijvoorbeeld, `Controlled Rz` is de beheerde versie van de `Rz` bewerking. 
`Rz`heeft type `((Double, Qubit) => Unit is Adj + Ctl)` , dus `Controlled Rz` heeft type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Dit is dus `Controlled Rz(controls, (0.1, target))` een geldige aanroep van `Controlled Rz` (Let op de haakjes rond `0.1, target` ).

Een ander voor beeld `CNOT(control, target)` kan worden geïmplementeerd als `Controlled X([control], target)` . Als een doel moet worden beheerd door twee Control qubits (CCNOT), gebruikt u een- `Controlled X([control1, control2], target)` instructie.

#### `Controlled Adjoint` 

Het `Controlled` en `Adjoint` functors werk, dus er is geen verschil tussen het Toep assen van `Controlled Adjoint Op` of `Adjoint Controlled Op` .


## <a name="defining-controlled-and-adjoint-implementations"></a>Beheerde en adjoint-implementaties definiëren

In de eerste declaratie van de bewerking in de vorige voor beelden `BitFlip` zijn de bewerkingen en `DecodeSuperdense` zijn gedefinieerd met hand tekeningen `(Qubit => Unit)` en `((Qubit, Qubit) => (Result, Result))` respectievelijk.
Net als bij `DecodeSuperdense` metingen, is het geen unitary-bewerking en zijn er geen beheerde niet-adjointe specials mogelijk (roep de gerelateerde vereiste in die een dergelijke bewerking retourneert `Unit` ).
Als `BitFlip` simpelweg de unitary <xref:microsoft.quantum.intrinsic.x> -bewerking uitvoert, kunt u deze echter ook met beide specials hebben gedefinieerd.

In deze sectie wordt beschreven hoe u het bestaan van specials in uw Q# bewerkings declaraties opneemt, waardoor u de mogelijkheid hebt om in combi natie met de of functors te worden aangeroepen `Adjoint` `Controlled` .
Zie voor meer informatie over een aantal situaties waarin het geldig is of niet geldig is voor het declareren van bepaalde specialies, de [omstandigheden voor het op geldige wijze definiëren van specials](#circumstances-for-validly-defining-specializations) in dit artikel.

De bewerkings kenmerken bepalen welke soorten functors u kunt Toep assen op de gedeclareerde bewerking en welk effect ze hebben. Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking, met name door een aantekening met de bewerkings kenmerken: ofwel `is Adj` , `is Ctl` of `is Adj + Ctl` .
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
Daarom kunt u deze gebruiken om de `DecodeSuperdense` in het vorige voor beeld compacter te schrijven, door gebruik te maken van de adjoint van `PrepareEntangledPair` om de Entangled-status terug te zetten in een unentangled paar qubits:

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

De aantekening met de bewerkings kenmerken in de declaratie is handig om ervoor te zorgen dat de compiler automatisch andere specials wordt gegenereerd op basis van de standaard implementatie. 

Er zijn enkele belang rijke beperkingen bij het ontwerpen van bewerkingen voor gebruik met functors.
De meeste van de voor delen van een bewerking die de uitvoer waarde van een andere bewerking gebruikt, *kan niet* automatisch worden gegenereerd door de compiler, omdat het niet eenduidig is hoe u de instructies in een dergelijke bewerking opnieuw ordent om hetzelfde effect te verkrijgen.

Daarom is het vaak handig om de verschillende implementaties expliciet op te geven.

### <a name="explicitly-specifying-implementations"></a>Expliciet opgeven van implementaties

Als de compiler de implementatie niet kan genereren, kunt u deze expliciet opgeven. Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte instructie voor het *genereren* of een door de gebruiker gedefinieerde implementatie.
Hieronder vindt u het volledige aanbod van mogelijkheden, met enkele voor beelden van expliciete specialisatie. 


#### <a name="explicit-specialization-declarations"></a>Expliciete specialisatie declaraties

Q#bewerkingen kunnen de volgende expliciete specialisatie declaraties bevatten:

- De `body` specialisatie specificeert de implementatie van de bewerking waarvoor geen functors is toegepast.
- De `adjoint` specialisatie specificeert de implementatie van de bewerking waarop de `Adjoint` functor is toegepast.
- De `controlled` specialisatie specificeert de implementatie van de bewerking waarop de `Controlled` functor is toegepast.
- De `controlled adjoint` specialisatie specificeert de implementatie van de bewerking waarbij de `Adjoint` en `Controlled` functors zijn toegepast.
  Deze specialisatie kan ook worden genoemd `adjoint controlled` , omdat de twee functors werkend zijn.


Een specialisatie bewerking bestaat uit de specialisatie code (bijvoorbeeld `body` of `adjoint` ), gevolgd door een van de volgende opties:

- Een expliciete declaratie zoals beschreven in het volgende.
- Een *instructie* die de compiler vertelt *hoe* de specialisatie moet worden gegenereerd, een van de volgende opties:
  - `intrinsic`. Dit geeft aan dat de doel computer de specialisatie levert.
  - `distribute`, gebruikt met de `controlled` and- `controlled adjoint` specials.
    Bij gebruik met `controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door toe `Controlled` te passen op alle bewerkingen in de `body` .
    Bij gebruik met `controlled adjoint` geeft dit aan dat de compiler de specialisatie moet berekenen door `Controlled` alle bewerkingen in de specialisatie toe te passen `adjoint` .
  - `invert`. Dit geeft aan dat de compiler de `adjoint` specialisatie moet berekenen door `body` bijvoorbeeld de volg orde van de bewerkingen te omkeren en de adjoint op elk ervan toe te passen.
    Bij gebruik met `adjoint controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door de specialisatie te omkeren `controlled` .
  - `self`om aan te geven dat de adjoint specialize hetzelfde is als de `body` specialisatie.
    Gebruik `self` is geldig voor de `adjoint` en `adjoint controlled` specials.
    Voor `adjoint controlled` `self` betekent dat de `adjoint controlled` specialisatie hetzelfde is als de `controlled` specialisatie.
  - `auto`om aan te geven dat de compiler een geschikte richt lijn moet selecteren om toe te passen.
    U kunt niet gebruiken `auto` voor de `body` specialisatie.

De richt lijnen en `auto` alle vereisen een sluitende punt komma `;` .
De `auto` instructie wordt omgezet in de volgende gegenereerde instructie als een expliciete declaratie van de `body` is geleverd:

- De `adjoint` specialisatie wordt gegenereerd volgens de instructie `invert` .
- De `controlled` specialisatie wordt gegenereerd volgens de instructie `distribute` .
- De `adjoint controlled` specialisatie wordt gegenereerd op basis van de instructie `invert` als een expliciete declaratie voor `controlled` is opgegeven, maar niet een voor `adjoint` , en `distribute` anders.

> [!TIP]   
> Als een bewerking zelf adjoint is, geeft u expliciet de adjoint of de bewaakte adjoint-specialisatie op via de generatie-instructie `self` zodat de compiler gebruik van die informatie kan maken voor optimaliserings doeleinden.

Een specialisatie declaratie met een door de gebruiker gedefinieerde implementatie bestaat uit een argument tuple gevolgd door een instructie blok met de Q# code die de specialisatie implementeert.
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

In het vorige `PrepareEntangledPair` voor beeld is de code gelijk aan de volgende code met expliciete specialisatie declaraties: 

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

Als de compiler de implementatie voor een bepaalde specialisatie niet automatisch kan genereren of als er een efficiëntere implementatie kan worden verleend, kunt u de implementatie hand matig definiëren.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
In het vorige voor beeld `adjoint invert;` geeft aan dat de adjoint-specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie te omkeren.

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

Het is wettelijk om een bewerking zonder adjoint of beheerde versies op te geven. Meting bewerkingen hebben bijvoorbeeld geen, omdat ze niet worden omkeerbaar of niet meer kunnen worden bestuurd.

Een bewerking ondersteunt de `Adjoint` en `Controlled` functors als de bijbehorende declaratie een impliciete of expliciete declaratie van de respectieve specials bevat.

Een expliciet aangegeven adjoint/beheerde specialisatie impliceert dat er een adjoint/beheerde specialisatie bestaat. 

Voor een bewerking waarvan de hoofd tekst herhalen-until-success-lussen, set-instructies, metingen, retour overzichten of aanroepen naar andere bewerkingen die de functor niet ondersteunen `Adjoint` , het automatisch genereren van een adjoint-specialisatie volgens de `invert` or- `auto` instructie is niet mogelijk.

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die de `Controlled` functor niet ondersteunen, is het automatisch genereren van een gecontroleerde specialisatie volgens de `distribute` or- `auto` instructie niet mogelijk.

#### <a name="controlled-adjoint"></a>Beheerde adjoint

In de gecontroleerde adjoint-versie van een bewerking wordt aangegeven hoe u een door een Quantum beheerde versie van de adjoint van de bewerking implementeert.
Het is niet toegestaan een bewerking op te geven zonder beheerde adjoint-versie. meting bewerkingen hebben bijvoorbeeld geen beheerde adjoint-versie omdat ze niet kunnen worden ingesteld of omkeerbaar.

Een beheerde adjoint-specialisatie voor een bewerking moet bestaan als en alleen als zowel een adjoint als een beheerde specialisatie bestaan. In dat geval wordt het bestaan van de beheerde adjoint-specialisatie afgeleid. Als er geen implementatie expliciet is gedefinieerd, genereert de compiler een geschikte specialisatie.

Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen beheerde adjoint-versie hebben, wordt het automatisch genereren van een adjoint-specialisatie volgens de `invert` , `distribute` of- `auto` instructie niet mogelijk.


### <a name="type-compatibility"></a>Type compatibiliteit

Gebruik een bewerking met aanvullende functors die overal worden ondersteund. u gebruikt een bewerking met minder functors maar dezelfde hand tekening. Gebruik bijvoorbeeld een bewerking van het type `(Qubit => Unit is Adj)` overal waar u een bewerking van type gebruikt `(Qubit => Unit)` .

Q#is *covariantie* ten opzichte van aanroep bare retour typen: een aanroepable die een type retourneert `'A` , is compatibel met een aanroepbaar met hetzelfde invoer type en een resultaat type dat compatibel is met `'A` .

Q#is *contra variant* ten opzichte van invoer typen: een aanroepable die een type `'A` als invoer vereist, is compatibel met een aanroepbaar met hetzelfde resultaat type en een invoer type dat compatibel is met `'A` .

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

U kunt

- Roep de functie `ConjugateInvertWith` aan met een `inner` argument van ofwel `Invert` of `ApplyUnitary` .
- Roep de functie `ConjugateUnitaryWith` aan met een `inner` argument van `ApplyUnitary` , maar niet `Invert` .
- Retourneert een waarde van het type `(Qubit[] => Unit is Adj + Ctl)` van `ConjugateInvertWith` .

> [!IMPORTANT]
> Q#0,3 heeft een aanzienlijk verschil in het gedrag van door de gebruiker gedefinieerde typen geïntroduceerd.

Door de gebruiker gedefinieerde typen worden behandeld als een ingepakte versie van het onderliggende type, in plaats van als subtype.
Dit betekent dat een waarde van een door de gebruiker gedefinieerd type niet kan worden gebruikt, waarbij u een waarde van het onderliggende type verwacht.


### <a name="conjugations"></a>Conjugations

In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn. Deze effecten kunnen worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven. Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende: 

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

Vanaf onze 0,9-release Q# ondersteunt een conjugation-instructie waarmee de voor gaande trans formatie wordt geïmplementeerd. Met deze instructie kan de bewerking `ApplyWith` op de volgende manier worden geïmplementeerd:

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
Een dergelijke conjugatione instructie is veel handiger als de buiten-en interne trans formaties niet direct beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies. 

De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid.
Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok. 


## <a name="defining-new-functions"></a>Nieuwe functies definiëren

Functions zijn louter deterministische, klassieke routines in Q# , die verschillen van bewerkingen in dat ze geen effect mogen hebben op de berekening van een uitvoer waarde.
Met name functies kunnen geen bewerkingen aanroepen; actie ondernemen, toewijzen of lenen qubits; voor beelden van wille keurige getallen; of op andere wijze, afhankelijk van de invoer waarde voor een functie.
Als gevolg hiervan Q# zijn functies *puur*, in die tijd dat ze altijd dezelfde invoer waarden toewijzen aan dezelfde uitvoer waarden.
Dit gedrag zorgt ervoor Q# dat de compiler veilig kan ordenen hoe en wanneer functies moeten worden aangeroepen bij het genereren van bewerkings-specials.

Elk Q# bron bestand kan elk wille keurig aantal functies definiëren.
Functie namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met bewerkingen of type namen.

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

Wanneer het mogelijk is om dit te doen, is het handig om klassieke logica te schrijven in termen van functies in plaats van bewerkingen, zodat u deze eenvoudig kunt gebruiken met bewerkingen. Als u bijvoorbeeld de eerdere `Square` declaratie als een *bewerking*had geschreven, zou de compiler niet kunnen garanderen dat het aanroepen van deze met dezelfde invoer dezelfde uitvoer zou produceren.

Als u het verschil tussen functies en bewerkingen wilt onderstrepen, moet u rekening houden met het probleem bij het klassiek bemonsteren van een wille keurig getal in een Q# bewerking:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Elke keer dat `U` deze wordt aangeroepen, heeft een andere actie op `target` .
Met name kan de compiler niet garanderen dat als u een `adjoint auto` specialisatie declaratie toevoegt aan `U` , vervolgens `U(target); Adjoint U(target);` fungeert als identiteit (dat wil zeggen, als niet-op).
Dit schendt de definitie van de adjoint die is gedefinieerd in [vectoren en matrices](xref:microsoft.quantum.concepts.vectors), waardoor de compiler automatisch een adjoint-specialisatie kan genereren in een bewerking waarbij u de bewerking aanroept <xref:microsoft.quantum.math.randomreal> , de door de compiler verstrekte garanties zou verstoren; <xref:microsoft.quantum.math.randomreal> is een bewerking waarvoor geen adjoint of gecontroleerde versie bestaat.

Aan de andere kant, zodat functie aanroepen zoals `Square` veilig zijn, en de compiler garandeert dat de invoer alleen moet worden behouden om de `Square` uitvoer stabiel te houden.
Door zo veel mogelijk klassieke logica in functies te isoleren, is het eenvoudig om die logica in andere functies en bewerkingen hetzelfde te hergebruiken.


## <a name="generic-type-parameterized-callables"></a>Algemene Callables (type parameters)

Veel functies en bewerkingen die u mogelijk wilt definiëren, zijn niet echt afhankelijk van de typen invoer, maar u kunt de typen echter alleen impliciet gebruiken via een andere functie of bewerking.
Stel dat het *kaart* concept gebruikelijk is in veel functionele talen. op basis van een functie $f (x) $ en een verzameling waarden $ \{ x_1, x_2, \dots, x_n \} $, kaart retourneert een nieuwe verzameling $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.
Als u dit in wilt implementeren, moet u Q# profiteren van het feit dat de functies voor de eerste klasse zijn.
Hier volgt een kort voor beeld van `Map` , met `T` als tijdelijke aanduiding wanneer u uitweet wat voor typen u nodig hebt.

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Houd er rekening mee dat deze functie veel hetzelfde lijkt, ongeacht de daad werkelijke typen die u vervangt.
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

In principe kunt u een versie van `Map` voor elk paar typen dat u tegen komt schrijven, maar dit heeft een aantal problemen.
Als u bijvoorbeeld een bug in hebt gevonden `Map` , moet u ervoor zorgen dat de oplossing op uniforme wijze wordt toegepast in alle versies van `Map` .
Als u bovendien een nieuwe tuple of UDT bouwt, moet u nu ook een nieuwe `Map` combi natie maken met het nieuwe type.
Hoewel dit kan worden beperkt door een klein aantal functies, kunt u, wanneer u meer en meer functies van hetzelfde formulier verzamelt `Map` , de kosten voor het introduceren van nieuwe typen in een redelijk korte volg orde onredelijk groot worden.

Veel van deze problemen kunnen er echter toe leiden dat u de compiler niet hebt gezien de informatie die nodig is om te bepalen hoe de verschillende versies van `Map` zijn gerelateerd.
Effectief wilt dat de compiler `Map` als een soort wiskundige functie van Q# *typen* naar functions wordt behandeld Q# .

Q#formalizes dit begrip door het toestaan van functies en bewerkingen om *type parameters*te hebben, evenals de normale tuple-para meters.
In de vorige voor beelden wilt u nadenken `Map` als having-para meters `Int, Pauli` in het eerste geval en `Double, String` in het tweede geval.
Voor het grootste deel gebruikt u deze type parameters alsof het normale typen zijn. Gebruik waarden van het type para meters om matrices en Tuples te maken, functies en bewerkingen aan te roepen en toe te wijzen aan gewone of onveranderlijke variabelen.

> [!NOTE]
> Het meest extreme geval van indirecte afhankelijkheid is die van qubits, waarbij een Q# programma niet rechtstreeks kan vertrouwen op de structuur van het `Qubit` type, maar **moet** dergelijke typen door geven aan andere bewerkingen en functies.

Teruggaan naar het vorige voor beeld. vervolgens ziet u dat u `Map` de para meters van het type moet hebben, een voor de invoer tot `fn` en met één om de uitvoer van weer te geven `fn` .
In Q# wordt dit geschreven door punt haken (dat wil zeggen `<>` , niet brakets $ \braket $!) toe te voegen {} na de naam van een functie of bewerking in de declaratie ervan en door elke type parameter te vermelden.
De naam van elke type parameter moet beginnen met een streepje `'` , wat aangeeft dat het een type parameter is en niet een normaal type (ook wel een *concreet* type genoemd).
Daarom `Map` is, geschreven:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Houd er rekening mee dat de definitie van `Map<'Input, 'Output>` lijkt extreem op de previoius-versies.
Het enige verschil is dat u de compiler expliciet hebt geïnformeerd dat `Map` niet direct afhankelijk is van wat `'Input` en dat `'Output` , maar wel voor twee typen, met behulp van deze indirect via `fn` .
Wanneer u `Map<'Input, 'Output>` op deze manier hebt gedefinieerd, kunt u deze aanroepen alsof het een gewone functie was:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Het schrijven van algemene functies en bewerkingen is een plek waar ' tuple-in ' tuple-out ' een zeer handige manier is om te denken over Q# functies en bewerkingen.
> Omdat elke functie precies één invoer heeft en er precies één uitvoer wordt geretourneerd, komt een invoer van het type `'T -> 'U` overeen met *een wille keurige* Q# functie.
> Op dezelfde manier kunt u een wille keurige bewerking door geven aan een invoer van het type `'T => 'U` .

Als tweede voor beeld moet u de uitdaging van het schrijven van een functie die de samen stelling van twee andere functies retourneert, overwegen:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier moet u precies opgeven wat `A` , `B` en `C` zijn, waardoor het hulp programma van de nieuwe functie aanzienlijk wordt beperkt `Compose` .
Daarna `Compose` is alleen afhankelijk van `A` , `B` en `C` *via* `innerFn` en `outerFn` .
Als alternatief kunt u vervolgens type parameters toevoegen aan `Compose` die aangeven dat het werkt voor *elk* `A` , `B` en, `C` zolang deze para meters overeenkomen met de verwachting door `innerFn` en `outerFn` :

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

De Q# standaard bibliotheken bieden een reeks dergelijke bewerkingen en functies van type para meters waarmee de controle stroom van een hogere volg orde eenvoudiger kan worden gemaakt.
Deze worden verder besproken in de [ Q# hand leiding standaard bibliotheek](xref:microsoft.quantum.libraries.standard.intro).


## <a name="callables-as-first-class-values"></a>Callables als waarden voor de eerste klasse

Een van de essentiële technieken voor het nemen van de controle stroom en klassieke logica met behulp van functies in plaats van bewerkingen is het gebruik van deze bewerkingen en functies in Q# *eerste klasse*.
Dat wil zeggen dat ze elke waarde in de taal in hun eigen recht zijn.
Het volgende is bijvoorbeeld een zeer geldige Q# code, als een beetje indirect:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

De waarde van de variabele `ourH` in het vorige code fragment is dan de bewerking <xref:microsoft.quantum.intrinsic.h> , zodat u die waarde als elke andere bewerking kunt aanroepen.
Met deze mogelijkheid kunt u bewerkingen schrijven waarmee bewerkingen worden uitgevoerd als onderdeel van de invoer en de concepten van de controle stroom met hogere volg orde vormen.
U kunt bijvoorbeeld Voorst Ellen om te ' Square ' een bewerking uit te laten lopen door deze twee keer op dezelfde doel-Qubit toe te passen.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Bewerkingen van een functie retour neren

Het is belang rijk om te benadrukken dat u ook bewerkingen als onderdeel van uitvoer kunt retour neren, zodat u sommige soorten klassieke voorwaardelijke logica kunt isoleren als een klassieke functie. deze retourneert een beschrijving van een Quantum programma in de vorm van een bewerking.
Als eenvoudig voor beeld kunt u het voor beeld van teleportie overwegen, waarbij de partij die een twee-bits klassiek bericht ontvangt, het bericht moet gebruiken om hun Qubit te decoderen naar de juiste teleportal-status.
U kunt dit schrijven in termen van een functie die deze twee klassieke bits accepteert en de juiste decodeer bewerking retourneert.

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

Deze nieuwe functie is inderdaad een functie. Als u deze aanroept met dezelfde waarden van `hereBit` en `thereBit` , krijgt u altijd dezelfde bewerking.
Zo kan de decoder veilig worden uitgevoerd binnen bewerkingen zonder dat dit de reden hoeft te zijn van de manier waarop de decoderings logica samenwerkt met de definities van de verschillende bewerkings-specials.
Dat wil zeggen dat de klassieke logica binnen een functie is geïsoleerd, zodat de compiler kan worden gevolgd met impunity, zolang de invoer wordt bewaard.


## <a name="partial-application"></a>Gedeeltelijke toepassing

U kunt aanzienlijk meer doen met functies die bewerkingen retour neren met behulp van *gedeeltelijke toepassing*, waarin u een of meer delen van de invoer voor een functie of bewerking kunt opgeven zonder dat u deze daad werkelijk aanroept. In het vorige `ApplyTwice` voor beeld kunt u aangeven dat u niet wilt opgeven, direct op welke Qubit de invoer bewerking moet worden toegepast:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In dit geval bevat de lokale variabele `twiceOp` de gedeeltelijk toegepaste bewerking `ApplyTwice(op, _)` , waarbij `_` delen van de invoer aangeeft die nog niet zijn opgegeven.
Wanneer u `twiceOp` op de volgende regel roept, geeft u als invoer aan de gedeeltelijk toegepaste bewerking alle resterende delen van de invoer aan de oorspronkelijke bewerking door.
Daarom is het voor gaande fragment in feite identiek aan het `ApplyTwice(op, target)` rechtstreeks aanroepen van, opslaan voor dat u een nieuwe lokale variabele hebt geïntroduceerd, zodat u de oproep kunt vertragen terwijl bepaalde onderdelen van de invoer worden verstrekt.

Omdat een bewerking die gedeeltelijk is toegepast, niet wordt aangeroepen totdat de volledige invoer is opgegeven, kunt u bewerkingen veilig Toep assen, zelfs binnen functies.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

In principe is de klassieke logica binnen `SquareOperation` mogelijk veel meer betrokken, maar is deze nog steeds geïsoleerd van de rest van een bewerking door de garanties dat de compiler over functies kan bieden. De Q# Standard-bibliotheek maakt gebruik van deze methode voor het uitdrukken van de klassieke controle stroom op een manier die kan worden gebruikt door Quantum Program ma's.


## <a name="recursion"></a>Recursie

Q#callables mogen direct of indirect recursief zijn.
Dat wil zeggen dat een bewerking of functie zichzelf kan aanroepen, of een andere aanroep kan aanroepen die direct of indirect de aanroep bare bewerking aanroept.

Er zijn twee belang rijke opmerkingen over het gebruik van recursie, echter:

- Het gebruik van recursie in bewerkingen heeft waarschijnlijk een conflict met bepaalde optimalisaties.
  Deze interferentie kan een grote invloed hebben op de uitvoerings tijd van de algoritme.
- Bij het uitvoeren van een echt Quantum apparaat kan de stack-ruimte beperkt zijn, waardoor een grondige recursie kan leiden tot een runtime-fout.
  Met name de Q# compiler en runtime identificeren en optimaliseren de staart recursie niet.

## <a name="next-steps"></a>Volgende stappen

Meer informatie over [variabelen](xref:microsoft.quantum.guide.variables) in Q# .