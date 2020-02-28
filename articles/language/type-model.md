---
title: 'Q #-gegevens typen'
description: 'Meer informatie over de verschillende typen die worden gebruikt in de Q #-programmeer taal, waaronder ingebouwde typen, matrices, Tuples, bewerkingen, functies en door de gebruiker gedefinieerde typen.'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 1fc4c0b3fed9277c7f9f3ac421330df03c1b30e4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904652"
---
# <a name="the-type-model"></a>Het type model

In deze sectie wordt het type Q # vermeld en wordt de syntaxis voor het opgeven en gebruiken van typen beschreven.
Houd er rekening mee dat Q # een *sterk getypeerde* taal is, zodat het gebruik van deze typen zorgvuldig kan bijdragen aan de compiler om sterke garanties te bieden voor Q #-Program ma's tijdens het compileren.

Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q # expliciet worden gebruikt voor het gebruik van aanroepen van functies die de conversie door lopen. Er zijn verschillende functies die deel uitmaken van de naam ruimte <xref:microsoft.quantum.convert>.
Er wordt impliciet een conversie naar compatibele typen uitgevoerd. 

Q # bevat beide primitieve typen, die rechtstreeks kunnen worden gebruikt en een aantal manieren om nieuwe typen van andere typen te maken.
We beschrijven elk in de rest van deze sectie.

## <a name="primitive-types"></a>Primitieve typen

De Q #-taal biedt verschillende *primitieve typen*, waaruit andere typen kunnen worden samengesteld:

- Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld: `2`, `107``-5`.
- Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, zoals `2L`, `107L``-5L`.
   Dit type is gebaseerd op de .NET-<xref:System.Numerics.BigInteger>
   voert.
- Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld: `0.0`, `-1.3``4e-7`.
- Het `Bool` type vertegenwoordigt een Booleaanse waarde die kan `true` of `false`zijn.
- Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.
   `Qubit`s ondoorzichtig zijn voor de gebruiker; de enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).
   Uiteindelijk worden acties op `Qubit`s geïmplementeerd door het aanroepen van intrinsieke instructies op een Quantum processor (of een simulatie daarvan).
- Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.
   Dit type wordt gebruikt voor het aanduiden van de basis bewerking voor rotaties en het bepalen van het waarneem bare gemeten.
   Dit is een genummerd type dat vier mogelijke waarden heeft: `PauliI`, `PauliX`, `PauliY`en `PauliZ`, die constanten van het type `Pauli`zijn.
- Het `Result` type vertegenwoordigt het resultaat van een meting.
   Dit is een opgesomd type met twee mogelijke waarden: `One` en `Zero`, die constanten zijn van het type `Result`.
   `Zero` geeft aan dat de + 1 eigenvalue is gemeten; `One` geeft de eigenvalue-1 aan.
- Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop`, waarbij de stap de opties zijn. 
   Dat `start .. stop` overeenkomt met `start..1..stop`, en bijvoorbeeld `1..2..7` vertegenwoordigt de reeks $\{1, 3, 5, 7\}$.
- Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.
  Dit type wordt gebruikt om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.
- Het `Unit` type is het type dat slechts één waarde `()`toestaat. 
  Dit type wordt gebruikt om aan te geven dat de functie van Q # of de bewerking geen informatie retourneert. 

De constanten `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`en `Zero` zijn alle gereserveerde symbolen in Q #.

## <a name="array-types"></a>Matrix typen

Als er een geldig Q #-type `'T`is, is er een type dat een matrix met waarden van het type `'T`vertegenwoordigt.
Dit matrix type wordt weer gegeven als `'T[]`; bijvoorbeeld `Qubit[]` of `Int[][]`.
Een verzameling integers wordt bijvoorbeeld aangeduid als `Int[]`, terwijl een matrix met matrices van `(Bool, Pauli)` waarden wordt aangegeven `(Bool, Pauli)[][]`.

In het tweede voor beeld ziet u dat dit een mogelijk gekartelde matrix van matrices is en niet een rechthoekige tweedimensionale matrix.
Q # biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.

Een matrix waarde kan worden geschreven in Q #-bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]`.
Het type van een matrix letterlijke waarde wordt bepaald door het algemene basis type van alle items in de matrix. 

> [!WARNING]
> De elementen van een matrix kunnen niet worden gewijzigd nadat de matrix is gemaakt.
> Instructies update-en-reassign en/of Copy-en-update-expressies kunnen worden gebruikt om een gewijzigde matrix te maken.

U kunt een matrix ook maken op basis van de grootte met behulp van het sleutel woord `new`:

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

In beide gevallen kan de functie kern `Length` worden gebruikt voor het verkrijgen van het aantal elementen als een `Int`wanneer een matrix is samengesteld.
Matrices kunnen worden ondergeschreven met behulp van vier Kante haken, met subscripts van het type `Int` of type `Range`om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.
De subscripts van matrices zijn gebaseerd op nul:

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>Tuple-typen

Als er een of meer verschillende typen `T0`, `T1`,..., `Tn`, kunnen we een nieuw *tuple-type* aanduiden als `(T0, T1, ..., Tn)`.
De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))`.
Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.

Waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.
`(3, false)` is bijvoorbeeld een tuple waarvan type het type tuple is `(Int, Bool)`.
Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.

Vanaf Q # 0,3 is `Unit` de naam van het *type* van de lege tuple. `()` wordt gebruikt voor de lege tuple- *waarde*.

Tuple-instanties zijn onveranderbaar.
Q # biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.

Tuples zijn een krachtig concept dat gedurende Q # wordt gebruikt voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.
Met name voor het gebruik van de tuple-notatie kunnen we uitdrukken dat elke bewerking en aanroepbaar precies één invoer hebben en er precies één uitvoer wordt geretourneerd.

### <a name="singleton-tuple-equivalence"></a>Singleton-tuple-equivalentie

Het is mogelijk om een singleton-tuple (single-element) te maken `('T1)`, zoals `(5)` of `([1,2,3])`.
Q # behandelt echter een singleton-tuple als volledig gelijk aan een waarde van het Inge sloten type.
Dat wil zeggen dat er geen verschil is tussen `5` en `(5)`, of tussen `5` en `(((5)))`, of tussen `(5, (6))` en `(5, 6)`.

Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.
Het is net zo geldig als het schrijven van `(5)+3` om `5+3`te schrijven en beide expressies evalueren om `8`.
Dit betekent met name dat een bewerking of functie waarvan het type tuple of uitvoer tuple één veld heeft, kan worden beschouwd als het nemen van één argument of het retour neren van een enkele waarde.

We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.

## <a name="user-defined-types"></a>Door de gebruiker gedefinieerde typen

Een Q #-bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.
Voor elk type tuple `T`kunnen we een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype`-instructie.
In de naam ruimte @"microsoft.quantum.math" worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:

```qsharp
newtype Complex = (Double, Double);
```

Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double`.   
Door de gebruiker gedefinieerde typen bieden geen ondersteuning voor anonieme items, ook wel vanaf Q # versie 0,7 of hoger. We hebben bijvoorbeeld de naam ' to items `Re` voor de dubbele waarde van het reële deel van een complex getal en `Im` voor het imaginaire deel: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund. Bovendien kunnen interne items ook een naam hebben.
Het type `Nested` zoals hieronder gedefinieerd, heeft bijvoorbeeld een onderliggend type `(Double, (Int, String))`, waarvan alleen het item van het type `Int` de naam heeft en alle andere items anoniem zijn. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de toegangs operator `::`. 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

Om toegang te krijgen tot anonieme items, moet de ingepakte waarde eerst worden geëxtraheerd met behulp van de achtervoegsel-operator `!`.
Met de operator ' uitpakken ', `!`, kunt u de waarde die is opgenomen in een door de gebruiker gedefinieerd type ophalen.
Het type van een dergelijke expressie voor ' uitpakken ' is het onderliggende type van het door de gebruiker gedefinieerde type. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

De operator voor het uitpakken van het uitpakken wordt één laag terugloop.
Meerdere opera tors voor uitpakken kunnen worden gebruikt om toegang te krijgen tot een waarde die is verpakt met vermenigvuldiging.

Bijvoorbeeld:

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

Bekijk de sectie over het [uitpakken van expressies](xref:microsoft.quantum.language.expressions#unwrap-expressions) en de [prioriteit van Opera tors](xref:microsoft.quantum.language.expressions#operator-precedence) voor meer informatie.

Waarden van een door de gebruiker gedefinieerd type kunnen worden gemaakt door de overeenkomende type-constructor aan te roepen:

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

U kunt ook nieuwe waarden maken op basis van bestaande, met behulp van [kopiëren-en-update-expressies](xref:microsoft.quantum.language.expressions#copy-and-update-expressions). Net als bij matrices kopieert deze expressies alle item waarden van de oorspronkelijke expressie, met uitzonde ring van de opgegeven benoemde items. Voor deze waarden worden ingesteld op die zijn gedefinieerd aan de rechter kant van de expressie. Alle andere taal constructies, zoals instructies voor [bijwerken en opnieuw toewijzen](xref:microsoft.quantum.language.statements#update-and-reassign-statement), die beschikbaar zijn voor matrix items bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

Door de gebruiker gedefinieerde typen kunnen worden gebruikt wanneer elk ander type kan worden gebruikt.
Het is met name mogelijk een matrix van een door de gebruiker gedefinieerd type te definiëren en een door de gebruiker gedefinieerd type op te geven als element van een tuple-type.

Het is niet mogelijk om recursieve type structuren te maken.
Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, mag geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.
Meer in het algemeen is het mogelijk dat door de gebruiker gedefinieerde typen geen cyclische afhankelijkheden hebben, waardoor de volgende reeks type definities ongeldig is:

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.
Als u terugkeert naar het voor beeld van `Complex`, kan één 2D polaire coördinaten ook als een door de gebruiker gedefinieerd type hebben gedefinieerd:

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

Hoewel zowel `Complex` als `Polar` een onderliggend type hebben `(Double, Double)`, zijn de twee typen volledig incompatibel in Q #, waarmee het risico wordt geminimaliseerd dat per ongeluk een complexe wiskundige functie aanroept met polaire coördinaten en omgekeerd.
Op deze manier hebben door de gebruiker gedefinieerde typen een vergelijk bare rol als records F# in bijvoorbeeld. 


## <a name="operation-and-function-types"></a>Bewerkings-en functie typen

Een Q #- _bewerking_ is een Quantum subroutine.
ofwel een aanroepbare routine die kwantumbewerkingen bevat.

Een Q #- _functie_ is een klassieke subroutine die wordt gebruikt binnen een Quantum algoritme.
Dit kan klassieke code bevatten, maar geen Quantum bewerkingen.
Met name kunnen functies geen qubits toewijzen of lenen en kunnen ze geen bewerkingen aanroepen.
Het is echter wel mogelijk om deze bewerkingen of qubits door te geven voor verwerking.
Functions zijn daarom volledig deterministisch in de zin dat het aanroepen van de argumenten altijd hetzelfde resultaat oplevert. 

Bewerkingen en functies worden samen _callables_genoemd.  Hieronder ziet u enkele [voor beelden](#examples) .

Alle Q # callables worden beschouwd als een enkele waarde als invoer en retour neren één waarde als uitvoer.
Zowel de invoer-als uitvoer waarden kunnen Tuples zijn.
Callables die geen resultaat retour `Unit`hebben.
Callables die geen invoer hebben, hebben de lege tuple als invoer.

Het basis type voor een aanroepable wordt geschreven als `('Tinput => 'Tresult)` of `('Tinput -> 'Tresult)`, waarbij zowel `'Tinput` als `'Tresult` typen zijn.
Het eerste formulier, met `=>`, wordt gebruikt voor bewerkingen. het tweede formulier, met `->`, voor functions.
`((Qubit, Pauli) => Result)` bijvoorbeeld vertegenwoordigt de hand tekening voor een mogelijke meting bewerking met één Qubit.

Functie typen zijn volledig opgegeven met hun hand tekening.
Een functie die de sinus van een hoek berekent, zou bijvoorbeeld het type `(Double -> Double)`hebben.

Bewerkingen, maar geen functies, hebben bepaalde extra _kenmerken_ die worden weer gegeven als onderdeel van het bewerkings type. Dergelijke kenmerken bevatten informatie over de functors die door de bewerking wordt ondersteund.
Functors zijn meta bewerkingen die een specialisatie van een basis bewerking genereren. Zie [functors](#functors)hieronder.

Bewerkings typen worden opgegeven door het invoer type, het uitvoer type en hun eigenschappen.    
Om ondersteuning te vereisen voor de `Controlled` en/of `Adjoint` functor in een bewerkings type, moeten we een aantekening toevoegen die de bijbehorende kenmerken aangeeft.
Een aantekening `is Ctl` bijvoorbeeld geeft aan dat de bewerking kan worden bestuurd. Als we willen vereisen dat een bewerking van dat Type zowel de `Adjoint` als `Controlled` functor ondersteunt, kunnen we dit als `(Qubit => Unit is Adj + Ctl)`uitdrukken. De gebruikte bewerkings kenmerken `Adj` en `Ctl` strikt uitspreken zijn twee vooraf gedefinieerde sets labels, waarbij elk label een bepaalde bewerkings kenmerken aangeeft, zoals bijvoorbeeld ondersteuning voor een bepaald functor.
`+` wordt dus gebruikt om de samen voeging van deze twee sets aan te geven en `*` wordt gebruikt om het snij punt aan te geven, bijvoorbeeld de labels die voor beide sets gelden.  

De Pauli-bewerking `X` heeft bijvoorbeeld type `(Qubit => Unit is Adj + Ctl)`.
Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.


### <a name="type-parameterized-functions-and-operations"></a>Functies en bewerkingen van het type para meters

Aanroep bare typen kunnen type parameters bevatten.
Type parameters worden aangeduid met een symbool dat wordt voorafgegaan door één aanhalings teken. `'A` is bijvoorbeeld een geldige type parameter.

Een type parameter kan meermaals voor komen in één hand tekening.
Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, zou hand tekening `(('A[], 'A->'A) -> 'A[])`hebben.
Op dezelfde manier kan een functie die de samen stelling van twee bewerkingen retourneert, een hand tekening hebben `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.

Bij het aanroepen van een type geparametriseerde aanroepable moeten alle argumenten van hetzelfde type para meter van hetzelfde type zijn.

Q # biedt geen mechanisme voor het beperken van de mogelijke typen die voor een type parameter kunnen worden vervangen.

### <a name="type-compatibility"></a>Type compatibiliteit

Een bewerking met aanvullende functors-ondersteuning kan worden gebruikt op een wille keurige locatie met minder functors, maar dezelfde hand tekening wordt verwacht.
Een bewerking van het type `(Qubit => Unit is Adj)` kan bijvoorbeeld worden gebruikt overal een bewerking van het type `(Qubit => Unit)` wordt verwacht.

Q # is covariantie ten opzichte van aanroep bare retour typen: een aanroepable die een type `'A` retourneert, is compatibel met een aanroepbaar met hetzelfde invoer type en een resultaat type dat `'A` compatibel is met.

Q # is contra variant met betrekking tot invoer typen: een aanroepable die een type `'A` als invoer compatibel is met een aanroepbaar met hetzelfde resultaat type en een invoer type dat compatibel is met `'A`.

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

- De functie `ConjugateInvertWith` kan worden aangeroepen met een `inner` argument van `Invert` of `ApplyUnitary`.
- De functie `ConjugateUnitaryWith` kan worden aangeroepen met een `inner` argument van `ApplyUnitary`, maar niet `Invert`.
- Een waarde van het type `(Qubit[] => Unit is Adj + Ctl)` kan worden geretourneerd vanuit `ConjugateInvertWith`.

> [!IMPORTANT]
> Q # 0,3 introduceert een aanzienlijk verschil in het gedrag van door de gebruiker gedefinieerde typen.

Door de gebruiker gedefinieerde typen worden behandeld als een ingepakte versie van het onderliggende type, in plaats van als subtype.
Dit betekent dat een waarde van een door de gebruiker gedefinieerd type niet kan worden gebruikt als een waarde van het onderliggende type wordt verwacht.

### <a name="functors"></a>Functors

Een functor in Q # is een Factory die een nieuwe bewerking vanuit een andere bewerking definieert.
Functors hebben toegang tot de implementatie van de basis bewerking bij het definiëren van de implementatie van de nieuwe bewerking.
Daarom kunnen functors complexere functies uitvoeren dan traditionele functies op een hoger niveau.

Functors hebben geen weer gave in het Q #-type systeem. Het is dus niet mogelijk om deze aan een variabele te binden of als argumenten door te geven. 

Een functor wordt gebruikt door deze toe te passen op een bewerking en een nieuwe bewerking te retour neren.
De bewerking die het resultaat is van het Toep assen van de `Adjoint` functor aan de `Y` bewerking wordt bijvoorbeeld geschreven als `Adjoint Y`.
De nieuwe bewerking kan vervolgens worden aangeroepen, zoals elke andere bewerking.
`Adjoint Y(q1)` past de adjoint functor toe aan de `Y` bewerking om een nieuwe bewerking te genereren en past die nieuwe bewerking toe op `q1`.

Op dezelfde manier `Controlled X(controls, target)` de beheerde functor toegepast op de `X` bewerking om een nieuwe bewerking te genereren en wordt die nieuwe bewerking toegepast op `controls` en `target`.

De twee standaard functors in Q # zijn `Adjoint` en `Controlled`.

#### <a name="adjoint"></a>Adjoint

In de Quantum Computing is de adjoint van een bewerking de complexe geconjugeerde omzetting van de bewerking.
Voor bewerkingen waarbij een unitary-operator wordt geïmplementeerd, is de adjoint de inverse van de bewerking.
Voor een eenvoudige bewerking die zojuist een reeks andere unitary-bewerkingen op een set qubits aanroept, kan de adjoint worden berekend door de adjoints van de subbewerkingen op dezelfde qubits toe te passen in de omgekeerde volg orde.

Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Adjoint` functor.
`Adjoint QFT` wijst bijvoorbeeld de adjoint van de `QFT` bewerking.
De nieuwe bewerking heeft dezelfde hand tekening en type als de basis bewerking.
Met name maakt de nieuwe bewerking ook gebruik van `Adjoint`en staat `Controlled` alleen toe als de basis bewerking is uitgevoerd.

De adjoint-functor is zijn eigen inverse; dat wil zeggen dat `Adjoint Adjoint Op` altijd hetzelfde is als `Op`.

#### <a name="controlled"></a>Gelijkrichter

De gecontroleerde versie van een bewerking is een nieuwe bewerking waarbij de basis bewerking alleen effectief wordt toegepast als alle besturings elementen qubits een opgegeven status hebben.
Als het besturings element qubits zich in de superpositie bevindt, wordt de basis bewerking samenhangend toegepast op het juiste deel van de superpositie.
Daarom worden beheerde bewerkingen vaak gebruikt voor het genereren van Entanglement.

In Q # maken bewaakte versies altijd een matrix van besturings element qubits, en de opgegeven status is altijd voor alle besturings elementen qubits in de status berekening (`PauliZ`) `One`, $ \ket{1}$.
Het beheer op basis van andere Staten kan worden bereikt door de juiste unitary-bewerking toe te passen op de controle qubits vóór de gecontroleerde bewerking en vervolgens de inverse van de unitary-bewerking toe te passen na de gecontroleerde bewerking.
Als u bijvoorbeeld een `X` bewerking toepast op een besturings element Qubit vóór en na een beheerde bewerking, zal de bewerking de `Zero` status ($ \ket{0}$) voor die Qubit beheren. het Toep assen van een `H` bewerking vóór en na gaat de `PauliX` `One` status, dat wil zeggen-1 eigenvalue van Pauli X, $ \ket{-} \mathrel{: =} (\ket{0}-\ket{1})/\sqrt{2}$ in plaats van de `PauliZ` `One` status.

Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Controlled` functor.
De hand tekening van de nieuwe bewerking is gebaseerd op de hand tekening van de oorspronkelijke bewerking.
Het resultaat type is hetzelfde, maar het invoer type is een twee-tuple met een Qubit-matrix met de Qubit (s) die het eerste element bevat en de argumenten van de oorspronkelijke bewerking als het tweede element.
De nieuwe bewerking ondersteunt `Controlled`en ondersteunt `Adjoint` alleen als de oorspronkelijke bewerking wordt uitgevoerd.

Als de oorspronkelijke bewerking slechts één argument heeft gevolgd, komt de singleton-tuple-equivalentie hier te staan.
`Controlled X` is bijvoorbeeld de bewaakte versie van de `X` bewerking.
`X` is van het type `(Qubit => Unit is Adj + Ctl)`, dus `Controlled X` heeft type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; vanwege Singleton-tuple-equivalentie is dit hetzelfde als `((Qubit[], Qubit) => Unit is Adj + Ctl)`.

Als de basis bewerking meerdere argumenten heeft, moet u de overeenkomstige argumenten van de gecontroleerde versie van de bewerking tussen haakjes plaatsen om ze te converteren naar een tuple.
`Controlled Rz` is bijvoorbeeld de bewaakte versie van de `Rz` bewerking.
`Rz` is van het type `((Double, Qubit) => Unit is Adj + Ctl)`, dus `Controlled Rz` heeft type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.
`Controlled Rz(controls, (0.1, target))` zou dus een geldige aanroep zijn van `Controlled Rz` (Let op de haakjes rond `0.1, target`).

Een ander voor beeld: `CNOT(control, target)` kan worden geïmplementeerd als `Controlled X([control], target)`. Als een doel moet worden beheerd door 2 Control qubits (CCNOT), kunnen we `Controlled X([control1, control2], target)`-instructie gebruiken.

### <a name="examples"></a>Voorbeelden

Dit voor beeld van een Q #-bewerking is afkomstig uit het voor beeld van de [meting](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) . Binnen bewerkingen kunnen we qubits toewijzen en Quantum bewerkingen gebruiken op deze qubits, zoals `H` en `X`:

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit() : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit
            set result = M(qubit);      // Measure the qubit
            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

Dit voor beeld van een functie is afkomstig uit het [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) -voor beeld. Het bevat louter klassieke code. U kunt zien dat, in tegens telling tot het bovenstaande voor beeld, geen qubits worden toegewezen en er geen Quantum bewerkingen worden gebruikt.

```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function PointwiseProduct(left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

Het is ook mogelijk dat een functie qubits kan worden door gegeven voor verwerking, zoals in dit voor beeld van het [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) -voor beeld. Qubits worden door gegeven aan de functie en worden gebruikt voor de verwerking, maar op geen enkel moment zijn de Qubit-statussen zelf gewijzigd.

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates(
    qubits : Qubit[], 
    masks : MCMTMask[]) 
: MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
