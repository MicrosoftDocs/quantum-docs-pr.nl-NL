---
title: Typen in Q#
description: Meer informatie over de verschillende typen die in de Q# programmeer taal worden gebruikt.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: c4a3e6563b8cabee87d1db6b9cb1c1f1c1a7131b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835822"
---
# <a name="types-in-no-locq"></a>Typen in Q#

In dit artikel worden het Q# type model en de syntaxis voor het opgeven en werken met typen beschreven. Zie [type expressies](xref:microsoft.quantum.guide.expressions)voor meer informatie over het maken en uitvoeren van expressies van deze typen.

Q#Het is een *sterk getypeerde* taal, zodat het gebruik van deze typen zorgvuldig kan helpen de compiler om sterke garanties te bieden voor Q# Program ma's tijdens het compileren.
Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q# expliciet worden aangeroepen met behulp van aanroepen naar functions die deze converteren. 
Q# biedt diverse functies als onderdeel van de <xref:microsoft.quantum.convert> naam ruimte.
Een upcast naar compatibele typen, anderzijds gebeurt impliciet. 

Q# biedt zowel primitieve typen, die rechtstreeks worden gebruikt, als verschillende manieren om nieuwe typen van andere typen te maken.
We beschrijven elk in de rest van dit artikel.

## <a name="primitive-types"></a>Primitieve typen

De Q# taal biedt de volgende *primitieve typen*, die allemaal rechtstreeks in Program ma's kunnen worden gebruikt Q# . U kunt deze primitieve typen ook gebruiken om nieuwe typen te maken.

- Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld,, `2` `107` , `-5` .
- Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, bijvoorbeeld,, `2L` `107L` `-5L` .
   Dit type is gebaseerd op .NET <xref:System.Numerics.BigInteger>
   voert.

- Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld, `0.0` , `-1.3` , `4e-7` .
- Het `Bool` type vertegenwoordigt een Booleaanse waarde van ofwel `true` of `false` .
- Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop` , waarbij de stap optioneel wordt aangeduid. 
   Bijvoorbeeld, `start .. stop` correspondeert met `start..1..stop` en `1..2..7` staat voor de reeks $ \{ 1, 3, 5, 7 \} $.
- Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.
  Gebruik het `string` type om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.
- Het `Unit` type kan slechts één waarde hebben, `()` . 
  Gebruik dit type om aan te geven dat Q# er geen gegevens worden geretourneerd door een functie of bewerking. 
- Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.
   `Qubit`s ondoorzichtig voor de gebruiker. De enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).
   Uiteindelijk implementeert u acties op `Qubit` s door het aanroepen van intrinsieke instructies op een Quantum processor (of een Quantum Simulator).
- Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.
   Gebruik dit type om de basis bewerking voor rotaties aan te duiden en het waarneem bare gemeten te bepalen.
   Het is een opgesomd type met vier mogelijke waarden: `PauliI` , `PauliX` , `PauliY` , en `PauliZ` , constanten van het type `Pauli` .
- Het `Result` type vertegenwoordigt het resultaat van een meting.
   Het is een opgesomd type met twee mogelijke waarden: `One` en `Zero` , die constanten van het type zijn `Result` .
   `Zero` geeft aan dat de + 1-eigenvalue is gemeten; `One` geeft aan dat de eigenvalue-1 is gemeten.

De constanten `true` , `false` ,,,,, `PauliI` `PauliX` `PauliY` `PauliZ` `One` en `Zero` zijn alle gereserveerde symbolen in Q# .

## <a name="array-types"></a>Matrix typen

* Voor elk geldig Q# type is er een type dat een matrix met waarden van dat type vertegenwoordigt.
    `Qubit[]`En `(Bool, Pauli)[]` vertegenwoordigen bijvoorbeeld matrices van `Qubit` waarden en `(Bool, Pauli)` tuple-waarden.

* Een matrix met matrices is ook geldig. Uitvouwen in het vorige voor beeld: er wordt een matrix met `(Bool, Pauli)` matrices aangeduid `(Bool, Pauli)[][]` .

> [!NOTE] 
> Dit voor beeld `(Bool, Pauli)[][]` vertegenwoordigt een mogelijk gekartelde matrix van matrices en geen rechthoekige tweedimensionale matrix. Q# biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.

* Een matrix waarde kan worden geschreven in Q# de bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]` .
Het algemene basis type van alle items in de matrix bepaalt het type van een matrix letterlijke waarde. Het maken van een matrix met elementen die geen gemeen schappelijk basis type hebben, veroorzaakt daarom een fout.  
Zie [matrices van callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables)voor een voor beeld.

    > [!WARNING]
    > Nadat de elementen van een matrix zijn gemaakt, kunnen ze niet meer worden gewijzigd.
    > Als u een aangepaste matrix wilt maken, gebruikt u de [instructies update-en-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) of [kopiëren-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).

* U kunt een matrix ook maken op basis van de grootte met behulp van het `new` sleutel woord:

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* Gebruik de functie kern `Length` om het aantal elementen van een matrix als een te verkrijgen `Int` .
* Matrices kunnen worden ondergeschreven om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.
De subscripts van matrices zijn gebaseerd op nul en moeten type `Int` of type zijn `Range` :

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a>Tuple-typen

Tuples zijn een krachtig concept dat door wordt gebruikt Q# voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.
Met name voor het gebruik van de tuple-notatie kunt u zien dat elke bewerking en aanroepable precies één invoer hebben en er precies één uitvoer wordt geretourneerd.

* Als er geen of meer verschillende typen `T0` , `T1` ,..., worden opgegeven, `Tn` kunt u een nieuw  *tuple-type* aanduiden als `(T0, T1, ..., Tn)` .
De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))` .
Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.

* De waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.
`(3, false)`Is bijvoorbeeld een tuple waarvan het type het type tuple is `(Int, Bool)` .
Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.

* Vanaf Q# 0,3, `Unit` is de naam van het *type* van de lege tuple; `()` wordt gebruikt voor de *waarde* van de lege tuple.

* Tuple-instanties zijn onveranderbaar.
Q# biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.



### <a name="singleton-tuple-equivalence"></a>Singleton-tuple-equivalentie

Het is mogelijk om een singleton-tuple (één element) `('T1)` te maken, zoals `(5)` of `([1,2,3])` .
Behandelt echter Q# een singleton-tuple als equivalent aan een waarde van het Inge sloten type.
Dat wil zeggen dat er geen verschil is tussen en `5` `(5)` , of tussen en of tussen en `5` `(((5)))` `(5, (6))` `(5, 6)` .
Het is net zo geldig als het schrijven van een `(5)+3` Schrijf bewerking `5+3` ; beide expressies evalueren naar `8` .

Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.
Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.
`(7)`Is bijvoorbeeld een expressie van het type `Int` , `([1,2,3])` is een expressie van het type `Int[]` en `((1,2))` is een expressie van het type `(Int, Int)` .

Dit betekent met name dat u een bewerking of functie kunt bekijken waarvan het type tuple of uitvoer tuple één veld heeft om één argument te maken of een enkele waarde te retour neren.

We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.


## <a name="user-defined-types"></a>Door de gebruiker gedefinieerde typen

Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype` , gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=` , een geldige type specificatie en een afsluitende punt komma.

Bijvoorbeeld:

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* Elk Q# bron bestand kan een wille keurig aantal door de gebruiker gedefinieerde typen declareren.
* Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.
* Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.
In het bijzonder is er geen automatische conversie tussen de waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.

### <a name="named-vs-anonymous-items"></a>Benoemde versus anonieme items

Een Q# bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.
Voor elk type tuple `T` kunt u een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype` instructie.
In de @"microsoft.quantum.math" naam ruimte worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:

```qsharp
newtype Complex = (Double, Double);
```
Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double` .   

Door de gebruiker gedefinieerde typen bieden ook ondersteuning voor *benoemde items* van anonieme items, vanaf Q# versie 0,7 of hoger. U kunt bijvoorbeeld de items een naam geven `Real` voor de dubbele waarde van het werkelijke deel van een complex getal en `Imag` voor het imaginaire deel: 

```qsharp
newtype Complex = (Real : Double, Imag : Double);
```
De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund. Daarnaast kunnen interne items ook een naam hebben.
Het type `Nested` , zoals hieronder gedefinieerd, heeft bijvoorbeeld een onderliggend type `(Double, (Int, String))` , waarvan alleen het item van het type de `Int` naam heeft en alle andere items anoniem zijn. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de *toegangs operator* `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Real + c2::Real, c1::Imag + c2::Imag);
}
```

Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.
Als u terugkeert naar het voor beeld van `Complex` , kan er een polaire coördinaten represenation zijn gedefinieerd als een door de gebruiker gedefinieerd type:

```qsharp
newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```

Hoewel beide `Complex` en `ComplexPolar` beide een onderliggend type hebben `(Double, Double)` , zijn de twee typen volledig incompatibel in Q# , waarmee het risico wordt geminimaliseerd dat per ongeluk een complexe wiskundige functie aanroept met polaire coördinaten en omgekeerd.

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Toegang tot anonieme items met de operator voor uitpakken

Als u toegang wilt krijgen tot anonieme items, moet u eerst de ingepakte waarde ophalen met de operator achtervoegsel `!` .
Met de operator ' uitpakken ' `!` kunt u de waarde die is opgenomen in een door de gebruiker gedefinieerd type extra heren.
Het type van een dergelijke expressie voor ' uitpakken ' is het onderliggende type van het door de gebruiker gedefinieerde type. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

Eén regel voor uitpakken van de operator deloopt één laag terugloop. Meerdere opera tors voor uitpakken gebruiken om toegang te krijgen tot een waarde met vermenigvuldiging.

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

Zie [type expressies in Q# ](xref:microsoft.quantum.guide.expressions)voor meer informatie over de operator voor uitpakken.

### <a name="creating-values-of-user-defined-types"></a>Waarden maken van door de gebruiker gedefinieerde typen

Maak waarden van een door de gebruiker gedefinieerd type door de bijbehorende type-constructor aan te roepen:

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

U kunt ook nieuwe waarden maken op basis van een bestaande waarde met behulp van [Copy-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions). Net zoals bij matrices, kopiëren-en-update-expressies worden alle item waarden van de oorspronkelijke expressie gekopieerd, met uitzonde ring van de opgegeven benoemde items. Voor deze uitzonde ringen zijn de waarden van deze items de waarden die aan de rechter kant van de expressie zijn gedefinieerd. Alle andere taal constructies die beschikbaar zijn voor matrix items, zoals [instructies update en opnieuw toewijzen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.

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

* U kunt door de gebruiker gedefinieerde typen overal gebruiken waar u andere typen gebruikt.
Het is met name mogelijk een matrix van een door de gebruiker gedefinieerd type te definiëren en een door de gebruiker gedefinieerd type op te geven als element van een tuple-type.

* Het is niet mogelijk om recursieve type structuren te maken.
Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, kan geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.
Meer in het algemeen zijn door de gebruiker gedefinieerde typen mogelijk geen cyclische afhankelijkheden van elkaar, waardoor de volgende sets type definities ongeldig zijn:

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a>Bewerkings-en functie typen

Op basis van de typen `'Tinput` en `'Tresult` :

* `('Tinput => 'Tresult)` is het basis type voor een wille keurige *bewerking*, bijvoorbeeld `((Qubit, Pauli) => Result)` .
* `('Tinput -> 'Tresult)` is het basis type voor een *functie*, bijvoorbeeld `(Int -> Int)` . 

Deze worden de *hand tekening* van de aanroepable genoemd.

* Alle Q# callables nemen één waarde als invoer en retour neren één waarde als uitvoer.
* U kunt Tuples gebruiken voor zowel de invoer-als uitvoer waarden.
* Callables die geen resultaat hebben, retour neren `Unit` .
* Callables die geen invoer hebben, hebben de lege tuple als invoer.

### <a name="functors"></a>Functors

*Functie* typen zijn volledig opgegeven met hun hand tekening. Een functie die bijvoorbeeld de sinus van een hoek berekent, zou type hebben `(Double -> Double)` . 

*Bewerkingen* hebben bepaalde extra kenmerken die worden weer gegeven als onderdeel van het bewerkings type. Dergelijke kenmerken bevatten informatie over welke *functors* de bewerking ondersteunt.
Als de uitvoering van de bewerking bijvoorbeeld afhankelijk is van de status van andere qubits, moet de functor worden ondersteund `Controlled` . als de bewerking een omgekeerde waarde heeft, moet de functor worden ondersteund `Adjoint` .

> [!NOTE]
> In dit artikel wordt alleen besproken hoe functors de hand tekening van de bewerking wijzigt. Zie [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie over functors en bewerkingen. 

Om ondersteuning voor de `Controlled` and/of `Adjoint` functor in een bewerkings type te vereisen, moet u een aantekening toevoegen die de bijbehorende kenmerken aangeeft.
De aantekening `is Ctl` (bijvoorbeeld `(Qubit => Unit is Ctl)` ) geeft aan dat de bewerking kan worden bestuurd. Dat wil zeggen dat de uitvoering afhankelijk is van de status van een andere Qubit of qubits. Op dezelfde manier wordt met de aantekening `is Adj` aangegeven dat de bewerking een adjoint heeft, dat wil zeggen, dat wil zeggen ' omgekeerd ', waardoor een bewerking herhaaldelijk wordt toegepast en de adjoint op een status de status ongewijzigd laat. 

Als u wilt vereisen dat een bewerking van dat Type zowel de als de `Adjoint` `Controlled` functor ondersteunt, kunt u dit als volgt uitdrukken `(Qubit => Unit is Adj + Ctl)` . De ingebouwde bewerking Pauli is bijvoorbeeld van het <xref:microsoft.quantum.intrinsic.x> type `(Qubit => Unit is Adj + Ctl)` . 

Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.

### <a name="type-parameterized-functions-and-operations"></a>Functies en bewerkingen van het type para meters

Aanroep bare typen kunnen *type parameters*bevatten.
Gebruik een symbool dat wordt voorafgegaan door één aanhalings teken om een type parameter te vermelden. `'A` is bijvoorbeeld een geldige type parameter.
Zie [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)voor meer informatie en informatie over het definiëren van type parameters callables.

Een type parameter kan meermaals voor komen in één hand tekening.
Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, heeft bijvoorbeeld de hand tekening `(('A[], 'A->'A) -> 'A[])` .
Op dezelfde manier heeft een functie die de samen stelling van twee bewerkingen retourneert, de hand tekening `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Wanneer u een aanroepable van het type para meter aanroept, moeten alle argumenten met dezelfde type parameter van hetzelfde type zijn.

Q# biedt geen methode voor het beperken van de mogelijke typen die een gebruiker kan vervangen door een type parameter.

## <a name="next-steps"></a>Volgende stappen

Nu u alle typen hebt gezien die de Q# taal vormen, Zie [ Q# expressies typen in](xref:microsoft.quantum.guide.expressions) voor meer informatie over het maken en bewerken van expressies van deze verschillende typen.
