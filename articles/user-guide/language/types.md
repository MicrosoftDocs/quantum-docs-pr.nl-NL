---
title: Typen in Q#
description: 'Meer informatie over de verschillende typen die worden gebruikt in de Q #-programmeer taal.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: f7a3ac3813966c0ef695068297ce4d9949ead554
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327285"
---
# <a name="types-in-q"></a>Typen in Q#

Op deze pagina wordt het type Q # vermeld en wordt de syntaxis voor het opgeven en werken met typen beschreven.
Op de volgende pagina [typt u expressies](xref:microsoft.quantum.guide.expressions), informatie over het maken en bewerken van expressies van deze typen.

Houd er rekening mee dat Q # een *sterk getypeerde* taal is, zodat het gebruik van deze typen zorgvuldig kan bijdragen aan de compiler om sterke garanties te bieden voor Q #-Program ma's tijdens het compileren.
Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q # expliciet worden gebruikt voor het gebruik van aanroepen van functies die de conversie door lopen. Er zijn verschillende functies die deel uitmaken van de <xref:microsoft.quantum.convert> naam ruimte.
Er wordt impliciet een conversie naar compatibele typen uitgevoerd. 

Q # bevat beide primitieve typen, die rechtstreeks kunnen worden gebruikt en een aantal manieren om nieuwe typen van andere typen te maken.
We beschrijven elk in de rest van deze sectie.

## <a name="primitive-types"></a>Primitieve typen

De Q #-taal biedt verschillende *primitieve typen*, waaruit andere typen kunnen worden samengesteld:

- Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld: `2` , `107` , `-5` .
- Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, bijvoorbeeld `2L` ,, `107L` `-5L` .
   Dit type is gebaseerd op .NET<xref:System.Numerics.BigInteger>
   voert.
- Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld: `0.0` , `-1.3` , `4e-7` .
- Het `Bool` type vertegenwoordigt een Booleaanse waarde die kan of zijn `true` `false` .
- Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop` , waarbij de stap optioneel wordt aangeduid. 
   Dit `start .. stop` komt overeen met `start..1..stop` , en geeft bijvoorbeeld `1..2..7` de reeks $ \{ 1, 3, 5, 7 \} $ aan.
- Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.
  Dit type wordt gebruikt om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.
- Het `Unit` type is het type waarmee slechts één waarde is toegestaan `()` . 
  Dit type wordt gebruikt om aan te geven dat de functie van Q # of de bewerking geen informatie retourneert. 
- Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.
   `Qubit`s ondoorzichtig voor de gebruiker; de enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).
   Uiteindelijk worden acties op `Qubit` s geïmplementeerd door het aanroepen van intrinsieke instructies op een Quantum processor (of een simulatie daarvan).
- Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.
   Dit type wordt gebruikt voor het aanduiden van de basis bewerking voor rotaties en het bepalen van het waarneem bare gemeten.
   Dit is een opgesomd type met vier mogelijke waarden: `PauliI` , `PauliX` , `PauliY` , en `PauliZ` , constanten van het type `Pauli` .
- Het `Result` type vertegenwoordigt het resultaat van een meting.
   Dit is een opgesomd type met twee mogelijke waarden: `One` en `Zero` , die constanten van het type zijn `Result` .
   `Zero`geeft aan dat de + 1-eigenvalue is gemeten; `One`Hiermee wordt de-1-eigenvalue aangegeven.

De constanten,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` en `Zero` zijn alle gereserveerde symbolen in Q #.

## <a name="array-types"></a>Matrix typen

Als er een geldig Q # `'T` -type is opgegeven, is er een type dat een matrix met waarden van het type vertegenwoordigt `'T` .
Dit matrix type wordt weer gegeven als `'T[]` , bijvoorbeeld `Qubit[]` of `Int[][]` .
Zo wordt bijvoorbeeld een verzameling met gehele getallen aangegeven `Int[]` , terwijl een matrix met `(Bool, Pauli)` waarden wordt aangeduid als matrix `(Bool, Pauli)[][]` .

In het tweede voor beeld ziet u dat dit een mogelijk gekartelde matrix van matrices is en niet een rechthoekige tweedimensionale matrix.
Q # biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.

Een matrix waarde kan worden geschreven in Q #-bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]` .
Het type van een matrix letterlijke waarde wordt bepaald door het algemene basis type van alle items in de matrix. Wanneer u probeert een matrix te maken met elementen die geen gemeen schappelijk basis type hebben, wordt er een fout gegenereerd.  
Zie [matrices van callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables) voor een voor beeld hiervan.

> [!WARNING]
> De elementen van een matrix kunnen niet worden gewijzigd nadat de matrix is gemaakt.
> [Instructies update-en-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) en/of [Copy-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) kunnen worden gebruikt om een gewijzigde matrix te maken.

U kunt een matrix ook maken op basis van de grootte met behulp van het `new` sleutel woord:

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

In beide gevallen kan de functie kern, wanneer een matrix is samengesteld, `Length` worden gebruikt om het aantal elementen als een te verkrijgen `Int` .
Matrices kunnen worden ondergeschreven met behulp van vier Kante haken, waarbij subscripts van `Int` het type of type `Range` zijn, om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.
De subscripts van matrices zijn gebaseerd op nul:

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>Tuple-typen

Nul of meer verschillende typen `T0` , `T1` ,..., `Tn` kunnen we een nieuw tuple- *type* aanduiden als `(T0, T1, ..., Tn)` .
De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))` .
Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.

Waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.
Bijvoorbeeld: `(3, false)` is een tuple waarvan het type het tuple-type is `(Int, Bool)` .
Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.

Vanaf Q # 0,3 `Unit` is de naam van het *type* van de lege tuple; `()` wordt gebruikt voor de lege tuple- *waarde*.

Tuple-instanties zijn onveranderbaar.
Q # biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.

Tuples zijn een krachtig concept dat gedurende Q # wordt gebruikt voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.
Met name voor het gebruik van de tuple-notatie kunnen we uitdrukken dat elke bewerking en aanroepbaar precies één invoer hebben en er precies één uitvoer wordt geretourneerd.

### <a name="singleton-tuple-equivalence"></a>Singleton-tuple-equivalentie

Het is mogelijk om een singleton-tuple (één element) te maken, `('T1)` zoals `(5)` of `([1,2,3])` .
Q # behandelt echter een singleton-tuple als volledig gelijk aan een waarde van het Inge sloten type.
Dat wil zeggen dat er geen verschil is tussen en `5` `(5)` , of tussen en of tussen en `5` `(((5)))` `(5, (6))` `(5, 6)` .
Het is net zo geldig als write `(5)+3` als schrijven `5+3` en beide expressies evalueren naar `8` .

Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.
Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.
Bijvoorbeeld: `(7)` is een `Int` expressie, `([1,2,3])` is een expressie van het type matrix van `Int` s en `((1,2))` is een expressie van het type `(Int, Int)` .

Dit betekent met name dat een bewerking of functie waarvan het type tuple of uitvoer tuple één veld heeft, kan worden beschouwd als het nemen van één argument of het retour neren van een enkele waarde.

We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.


## <a name="user-defined-types"></a>Door de gebruiker gedefinieerde typen

Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype` , gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=` , een geldige type specificatie en een afsluitende punt komma.

Bijvoorbeeld:

```qsharp
newtype PairOfInts = (Int, Int);
```

Elk Q #-bron bestand kan elk gewenst aantal door de gebruiker gedefinieerde typen declareren.
Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.

Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.
In het bijzonder is er geen automatische conversie tussen waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.

### <a name="named-vs-anonymous-items"></a>Benoemde versus anonieme items

Een Q #-bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.
Voor elk type tuple `T` kunnen we een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype` instructie.
In de @"microsoft.quantum.math" naam ruimte worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:

```qsharp
newtype Complex = (Double, Double);
```
Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double` .   

Door de gebruiker gedefinieerde typen ondersteunen ook *benoemde items* van anonieme items, vanaf Q # versie 0,7 of hoger. We hebben bijvoorbeeld de naam ' to items ' `Re` voor de dubbele waarde van het reële deel van een complex getal en `Im` voor het imaginaire deel: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund. Daarnaast kunnen interne items ook een naam hebben.
Het type `Nested` zoals hieronder gedefinieerd is bijvoorbeeld een onderliggend type `(Double, (Int, String))` , waarvan alleen het item van het type de `Int` naam heeft en alle andere items anoniem zijn. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de *toegangs operator* `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.
Als u terugkeert naar het voor beeld van `Complex` , kunt u een 2D polaire coördinaten ook als een door de gebruiker gedefinieerd type hebben gedefinieerd:

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

Hoewel beide `Complex` en `Polar` beide een onderliggend type hebben `(Double, Double)` , zijn de twee typen volledig incompatibel in Q #, zodat het risico wordt geminimaliseerd dat er per ongeluk een complexe wiskundige functie wordt aangeroepen met polaire coördinaten en omgekeerd.
Op deze manier hebben door de gebruiker gedefinieerde typen een vergelijk bare rol als records in F #, bijvoorbeeld. 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Toegang tot anonieme items met de operator voor uitpakken

Om toegang te krijgen tot anonieme items, moet de ingepakte waarde eerst worden geëxtraheerd met de operator achtervoegsel `!` .
De operator ' wrap ' `!` kan de waarde in een door de gebruiker gedefinieerd type ophalen.
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

Meer informatie over de operator voor uitpakken kunt u vinden [in type-expressies in Q #](xref:microsoft.quantum.guide.expressions).

### <a name="creating-values-of-user-defined-types"></a>Waarden maken van door de gebruiker gedefinieerde typen

Waarden van een door de gebruiker gedefinieerd type kunnen worden gemaakt door de overeenkomende type-constructor aan te roepen:

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

U kunt ook nieuwe waarden maken op basis van bestaande, met behulp van [kopiëren-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions). Net als bij matrices kopieert deze expressies alle item waarden van de oorspronkelijke expressie, met uitzonde ring van de opgegeven benoemde items. Voor deze waarden worden ingesteld op die zijn gedefinieerd aan de rechter kant van de expressie. Alle andere taal constructies, zoals [instructies update-and-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), die beschikbaar zijn voor matrix items bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.

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

Opmerking is niet mogelijk om recursieve type structuren te maken.
Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, mag geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.
Meer in het algemeen is het mogelijk dat door de gebruiker gedefinieerde typen geen cyclische afhankelijkheden hebben, waardoor de volgende reeks type definities ongeldig is:

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a>Bewerkings-en functie typen

Het basis type voor een aanroepable is geschreven als `('Tinput => 'Tresult)` of `('Tinput -> 'Tresult)` , waarbij beide `'Tinput` en `'Tresult` typen zijn.
Deze worden de *hand tekening* van de aanroepable genoemd.

Alle Q # callables worden beschouwd als een enkele waarde als invoer en retour neren één waarde als uitvoer.
Zowel de invoer-als uitvoer waarden kunnen Tuples zijn.
Callables die geen resultaat retour hebben `Unit` .
Callables die geen invoer hebben, hebben de lege tuple als invoer.

> [!NOTE]
> Het eerste formulier, met `=>` , wordt gebruikt voor bewerkingen; het tweede formulier, met `->` , voor functions.
> Bijvoorbeeld, `((Qubit, Pauli) => Result)` vertegenwoordigt de hand tekening voor een mogelijke meting bewerking met één Qubit.
*Functie* typen zijn volledig opgegeven met hun hand tekening.
Een functie die bijvoorbeeld de sinus van een hoek berekent, zou type hebben `(Double -> Double)` .

*Bewerkingen*---maar geen functies---bepaalde extra kenmerken hebben die worden weer gegeven als onderdeel van het bewerkings type. Dergelijke kenmerken bevatten informatie over de *functors* die door de bewerking wordt ondersteund.
Als de uitvoering van de bewerking bijvoorbeeld kan worden voor bereid op de status van andere qubits, moet deze de functor ondersteunen `Controlled` ; als de bewerking een omgekeerde waarde heeft, moet de functor worden ondersteund `Adjoint` . Functors en-bewerkingen worden gedetailleerd besproken bij [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions), maar hier bespreken we gewoon hoe de hand tekening van de bewerking verandert.

Om ondersteuning voor de `Controlled` and/of `Adjoint` functor in een bewerkings type te vereisen, moeten we een aantekening toevoegen die de bijbehorende kenmerken aangeeft.
Een aantekening `is Ctl` (bijvoorbeeld `(Qubit => Unit is Ctl)` ) geeft aan dat de bewerking kan worden bestuurd---dat wil zeggen dat de uitvoering wordt uitgevoerd voor de status van een andere Qubit of qubits. Op dezelfde manier `is Adj` wordt hiermee aangegeven dat de bewerking een adjoint heeft, of gewoon kan worden omgekeerd, waardoor een bewerking herhaaldelijk wordt toegepast en de adjoint naar een status de status ongewijzigd laat. 

Als we willen vereisen dat een bewerking van dat Type zowel de als de `Adjoint` `Controlled` functor ondersteunt, kunnen we dit als volgt uitdrukken `(Qubit => Unit is Adj + Ctl)` . De ingebouwde bewerking Pauli is bijvoorbeeld van het <xref:microsoft.quantum.intrinsic.x> type `(Qubit => Unit is Adj + Ctl)` . 

Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.

### <a name="type-parameterized-functions-and-operations"></a>Functies en bewerkingen van het type para meters

Aanroep bare typen kunnen type parameters bevatten.
Type parameters worden aangeduid met een symbool dat wordt voorafgegaan door één aanhalings teken. `'A`is bijvoorbeeld een geldige type parameter.
Details over het definiëren van type para meters callables worden gegeven op de pagina [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .

Een type parameter kan meermaals voor komen in één hand tekening.
Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, zou hand tekening zijn `(('A[], 'A->'A) -> 'A[])` .
Op dezelfde manier kan een functie die de samen stelling van twee bewerkingen retourneert, hand tekeningen hebben `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Bij het aanroepen van een type geparametriseerde aanroepable moeten alle argumenten van hetzelfde type para meter van hetzelfde type zijn.

Q # biedt geen mechanisme voor het beperken van de mogelijke typen die voor een type parameter kunnen worden vervangen.

## <a name="next-steps"></a>Volgende stappen

Nu u alle typen hebt gezien die de Q #-taal vormen, kunt u in het hoofd om [expressies in q # te typen](xref:microsoft.quantum.guide.expressions) om te zien hoe u expressies van deze verschillende typen maakt en bewerkt.


