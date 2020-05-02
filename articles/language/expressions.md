---
title: 'Q #-expressies'
description: 'Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q #.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683931"
---
# <a name="expressions"></a>Expressies

## <a name="grouping"></a>Shapes

Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.
Bijvoorbeeld `(7)` : is een `Int` expressie, `([1,2,3])` is een expressie van het type matrix van `Int`s en `((1,2))` is een expressie van het type `(Int, Int)`.

De equivalentie tussen eenvoudige waarden en enkele Tuples die in [het type model](xref:microsoft.quantum.language.type-model#tuple-types) worden beschreven, verwijdert de dubbel zinnigheid `(6)` tussen als een groep `(6)` en als een tuple met één element.

## <a name="symbols"></a>Symbolen

De naam van een symbool dat `'T` is gekoppeld aan of is toegewezen aan een waarde van het type `'T`, is een expressie van het type.
Als het symbool `count` bijvoorbeeld is gebonden aan de waarde `5`geheel getal, `count` is dit een expressie met gehele getallen.

## <a name="numeric-expressions"></a>Numerieke expressies

Numerieke expressies zijn expressies van het `Int`type `BigInt`, of `Double`.
Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.

`Int`letterlijke waarden in Q # zijn identiek aan letterlijke waarden in C#, behalve dat er geen ' l ' of ' L ' vereist is (of toegestaan).
Hexadecimale en binaire gehele getallen worden respectievelijk met het voor voegsel ' 0x ' en ' 0b ' ondersteund.

`BigInt`letterlijke waarden in Q # zijn identiek aan teken reeksen met een groot geheel getal in .NET, waarbij een ' l ' of ' L ' wordt gevolgd.
Hexadecimale Big-gehele getallen worden ondersteund met het voor voegsel 0x.
Daarom zijn de volgende geldige toepassingen van `BigInt` letterlijke waarden:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`letterlijke waarden in Q # zijn identiek aan dubbele letterlijke waarden in C#, behalve dat er geen ' d ' of ' D ' vereist is (of toegestaan).

Een `Int` expressie met een matrix expressie van elk element type kan worden gevormd met behulp `Length` van de ingebouwde functie, met de matrix expressie tussen haakjes `(` en. `)`
Als `a` bijvoorbeeld is gebonden aan een matrix, `Length(a)` is dit een expressie met gehele getallen.
Als `b` is een matrix met matrices van gehele getallen, `Int[][]` `Length(b)` is dit het aantal submatrixen in `b`en `Length(b[1])` is het aantal gehele getallen in de tweede submatrix in. `b`

Gegeven twee numerieke expressies van hetzelfde type, de binaire Opera tors `+`, `-` `*`, en `/` kunnen worden gebruikt om een nieuwe numerieke expressie te vormen.
Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.

Als u twee geheeltallige expressies hebt opgegeven, `^` kan de binaire operator (Power) worden gebruikt voor het maken van een nieuwe expressie met gehele getallen.
Dit `^` kan ook worden gebruikt met twee dubbele expressies om een nieuwe dubbele expressie te vormen.
Ten slotte `^` kan worden gebruikt met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant om een nieuwe Big Integer-expressie te vormen.
In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.

Als er twee integere of Big Integer-expressies zijn opgegeven, kan een nieuwe integer of Big Integer `%` -expressie worden gevormd met `&&&` behulp van de Opera `|||` tors (modulus), `^^^` (bitsgewijze en), (bitsgewijze OR) of (Bitsgewijze XOR).

Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de `<<<` rechter kant, de (reken `>>>` kundige Shift-toets links) of de Opera tors reken kundig naar rechts kan worden gebruikt om een nieuwe expressie te maken met hetzelfde type als de linker expressie.

De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.
Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.
Als het getal dat moet worden verplaatst een geheel getal is, wordt het verwerkings `mod 64`bedrag geïnterpreteerd. dat wil zeggen dat een verschuiving van 1 en een verschuiving van 65 hetzelfde effect hebben.

Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.
Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.
Dat wil zeggen dat de ene stap naar links of rechts verschuift precies hetzelfde is als vermenigvuldigen of delen met 2.

Geheel getal delen en integers modulus volgen hetzelfde gedrag voor negatieve getallen als C#.
Dat wil zeggen `a % b` , heeft altijd hetzelfde teken als `a`en `b * (a / b) + a % b` is altijd gelijk aan. `a`
Bijvoorbeeld:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 5 | 2 | -2 | -1
 5 | -2 | 2 | -1

Het delen van een groot geheel getal en modulus werkt op dezelfde manier.

Op basis van een numerieke expressie kan een nieuwe expressie worden gevormd met `-` behulp van de unaire operator.
De nieuwe expressie is van hetzelfde type als de component-expressie.

Een nieuwe expressie van hetzelfde type als een geheel getal of Big Integer-expressie kan worden gevormd met behulp van de `~~~` (bitsgewijze complement) monadische operator.

## <a name="boolean-expressions"></a>Booleaanse expressies

De twee `Bool` letterlijke waarden `true` zijn `false`en.

Op basis van twee expressies van hetzelfde primitieve type kunnen de en `==` `!=` binaire Opera tors worden gebruikt voor het maken van `Bool` een expressie.
De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.

Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken. Als u bijvoorbeeld de operator `!` ' teruglopen ' gebruikt (Zie de [pagina Q # type model](xref:microsoft.quantum.language.type-model#user-defined-types)),

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Gelijkheids vergelijking `Qubit` voor waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.
De status van de twee qubits wordt niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.

Gelijkheids vergelijking `Double` voor waarden kan misleiden door Afrondings effecten.
Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.

Met een wille keurige combi natie van `>`twee `<`numerieke `>=`expressies worden `<=` de binaire Opera Tors,, en kunnen worden gebruikt om een nieuwe booleaanse expressie te maken die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.

Aan de hand van twee Booleaanse expressies `and` kunnen `or` de en binaire Opera tors worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als beide (of beide) de twee expressies waar zijn.

Aan de hand van een Booleaanse `not` expressie kan de unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.

## <a name="string-expressions"></a>Teken reeks expressies

Q # Hiermee kunnen teken reeksen worden gebruikt in `fail` de instructie en `Log` de standaard functie.

Teken reeksen in Q # zijn letterlijke waarden of geïnterpoleerde teken reeksen.
Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks van Unicode-tekens tussen dubbele citaten, `"`.
In een teken reeks kan de back slash-teken `\` worden gebruikt om een dubbel aanhalings teken te escapen en om een nieuwe regel als `\n`een regel terugloop als `\r`en een tab in te voegen `\t`als.
Bijvoorbeeld:

```qsharp
"\"Hello world!\", she said.\n"
```

De syntaxis van Q # voor teken reeks-interpolatie is een subset van de C# 7,0-syntaxis. Q # biedt geen ondersteuning voor Verbatim-geïnterpoleerde teken reeksen (meerdere regels).
Zie [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) voor de C#-syntaxis.

Expressies binnen een geïnterpoleerde teken reeks volgen Q # syntaxis, geen C#-syntaxis.
Een geldige Q #-expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.

## <a name="qubit-expressions"></a>Qubit-expressies

De enige `Qubit` expressies zijn symbolen die zijn gebonden aan `Qubit` waarden of matrix elementen van `Qubit` matrices.
Er zijn geen `Qubit` letterlijke waarden.

## <a name="pauli-expressions"></a>Pauli-expressies

De vier `Pauli` waarden, `PauliI`, `PauliX` `PauliY`, en `PauliZ`zijn allemaal geldige `Pauli` expressies.

Behalve dat zijn de enige `Pauli` expressies symbolen die zijn gebonden aan `Pauli` waarden of matrix elementen van `Pauli` matrices.

## <a name="result-expressions"></a>Resultaat expressies

De twee `Result` waarden `One` en `Zero`zijn geldige `Result` expressies.

Behalve dat zijn de enige `Result` expressies symbolen die zijn gebonden aan `Result` waarden of matrix elementen van `Result` matrices.
Let er met name op `One` dat niet hetzelfde is als het gehele `1`getal en er geen rechtstreekse conversie tussen deze waarden is.
Hetzelfde geldt voor `Zero` en `0`.

## <a name="range-expressions"></a>Bereik expressies

Er zijn drie `Int` expressies `start`, `step`en `stop` `start .. step .. stop` , een bereik expressie waarvan `start`het eerste element, het tweede `start+step`element, het derde element is `start+step+step`, enzovoort, totdat `stop` het wordt door gegeven.
Een bereik kan leeg zijn als bijvoorbeeld positief `step` is en. `stop < start`
Het laatste element van het bereik `stop` wordt als het verschil tussen `start` en `stop` is een integraal veelvoud van; `step` dat wil zeggen dat het bereik op beide uiteinden is inbegrepen.

Als u twee `Int` expressies `start` opgeeft `stop`en `start .. stop` , is dit een bereik expressie die gelijk `start .. 1 .. stop`is aan.
Houd er rekening mee dat `step` de geïmpliceerde is + `stop` 1, zelfs `start`als deze kleiner is dan; in dat geval is het bereik leeg.

Enkele voor beelden van bereiken:

- `1..3`is het bereik van 1, 2, 3.
- `2..2..5`is het bereik van 2, 4.
- `2..2..6`is het bereik 2, 4, 6.
- `6..-2..2`is het bereik van 6, 4, 2.
- `2..1`is een leeg bereik.
- `2..6..7`is het bereik 2.
- `2..2..1`is een leeg bereik.
- `1..-1..2`is een leeg bereik.

## <a name="callable-expressions"></a>Aanroep bare expressies

Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.
`X` Bijvoorbeeld: is een letterlijke bewerkings bewerking die verwijst naar `X` de standaard- `Message` bibliotheek bewerking en is een functie-literal die verwijst `Message` naar de functie standaard bibliotheek.

Als een bewerking de `Adjoint` functor ondersteunt, `Adjoint op` is een bewerkings expressie.
Op dezelfde manier geldt dat als de `Controlled` bewerking de functor `Controlled op` ondersteunt, een bewerkings expressie is.
De typen van deze expressies worden opgegeven in [functors](xref:microsoft.quantum.language.type-model#functors).

Functors (`Adjoint` en `Controlled`) binden meer nauw keuriger dan alle andere opera Tors, met uitzonde `!` ring van de operator `[]`voor uitpakken en het indexeren van matrices met.
Daarom is het volgende juridisch, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

Een aanroep bare letterlijke tekenloze kan worden gebruikt als een waarde, moet worden toegewezen aan een variabele of door gegeven aan een andere aanroepable.
Als de aanroepable van het type para meters is, moeten deze als onderdeel van de aanroep bare waarde worden opgegeven.
Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben.

Als `Fun` bijvoorbeeld een functie met hand tekening `'T1->Unit`is:

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aanroep bare aanroepende expressies

Gezien een aanroep bare (Operation-of Function-) expressie en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kan een aanroep expressie worden gevormd door de tuple-expressie toe te voegen aan de aanroep bare expressie.
Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.

Als `Op` bijvoorbeeld een bewerking met hand tekening `((Int, Qubit) => Double)`is, `Op(3, qubit1)` is een expressie van het type `Double`.
Op dezelfde manier `Sin` is, als een functie `(Double -> Double)`met `Sin(0.1)` hand tekening, een expressie `Double`van het type.
Ten slotte, `Builder` als een functie met hand `(Int -> (Int -> Int))`tekening, `Builder(3)` is een functie van naar int.

Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.
Om het resultaat van aanroepen `Builder` vanuit de vorige alinea te kunnen aanroepen, is de juiste syntaxis:

```qsharp
(Builder(3))(2)
```

Bij het aanroepen van een aanroep bare type para meter kunnen de werkelijke type parameters worden opgegeven tussen punt haken `<` en `>` na de aanroep bare expressie.
Dit is doorgaans onnodig omdat de compiler Q # de daad werkelijke typen afleidt.
Het is vereist voor een gedeeltelijke toepassing (zie hieronder) als een argument van het type para meters niet-opgegeven is.
Het is ook soms handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.

Bijvoorbeeld `Func` als hand tekening `('T1, 'T2, 'T1) -> 'T2`is ondertekend, `Op1` `Op2` hand `(Qubit[] => Unit is Adj)`tekening heeft en `Op3` hand tekening `(Qubit[] => Unit)`heeft, om als `Func` het `Op1` eerste argument `Op2` als tweede en `Op3` als derde te worden aangeroepen:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

De type specificatie is vereist omdat `Op3` en `Op1` andere typen hebben, waardoor de compiler dit als dubbel zinnig wordt behandeld zonder de specificatie.

### <a name="partial-application"></a>Gedeeltelijke toepassing

Op basis van een aanroep bare expressie kan een nieuwe aanroep worden gemaakt door een subset van de argumenten op te geven die kunnen worden aangeroepen.
Dit wordt _gedeeltelijke toepassing_genoemd.

In Q # wordt een gedeeltelijk toegepaste aanroepable weer gegeven door een expressie met een gewone aanroep te schrijven, maar met een `_`onderstrepings teken, voor de niet-opgegeven argumenten.
De resulterende aanroepable heeft hetzelfde resultaat type als het basis aanroepable en dezelfde specialisatie voor bewerkingen.
Het invoer type van de gedeeltelijke toepassing is gewoon het oorspronkelijke type met de opgegeven argumenten verwijderd.

Als een onveranderlijke variabele wordt door gegeven als een opgegeven argument bij het maken van een gedeeltelijke toepassing, wordt de huidige waarde van de variabele gebruikt.
Als u de waarde van de variabele achteraf wijzigt, heeft dit geen invloed op de gedeeltelijke toepassing.

Als `Op` bijvoorbeeld het volgende type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`is:

- `Op(5,(_,_))`heeft het `(((Qubit,Qubit), Double) => Unit is Adj)`type en heeft `Op(5,_)`dus.
- `Op(_,(_,1.0))`heeft type `((Int, (Qubit,Qubit)) => Unit is Adj)`.
- `Op(_,((q1,q2),_))`heeft type `((Int,Double) => Unit is Adj)`.
   Let op: we hebben hier Singleton-tuple-equivalentie toegepast.

Als het gedeeltelijk toegepaste aanroep type para meters heeft die niet kunnen worden afgeleid door de compiler, moeten deze worden opgegeven op de aanroep site.
De gedeeltelijke toepassing mag geen niet-opgegeven type parameters hebben.

Als `Op` bijvoorbeeld het volgende type `(('T1, Qubit, 'T1) => Unit : Adjoint)`is:

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a>Recursie

Q # callables mogen direct of indirect recursief zijn.
Dat wil zeggen dat een bewerking of functie zichzelf kan aanroepen, of een andere aanroep kan aanroepen die direct of indirect de aanroep bare bewerking aanroept.

Er zijn twee belang rijke opmerkingen over het gebruik van recursie, echter:

- Het gebruik van recursie in bewerkingen heeft waarschijnlijk een conflict met bepaalde optimalisaties.
  Dit kan een aanzienlijke invloed hebben op de uitvoerings tijd van de algoritme.
- Bij het uitvoeren van een echt Quantum apparaat kan de stack-ruimte beperkt zijn en kan een grondige recursie leiden tot een runtime-fout.
  Met name de Q #-compiler en runtime identificeren en optimaliseren de staart recursie niet.

## <a name="tuple-expressions"></a>Tuple-expressies

Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen `(` en. `)`
Bijvoorbeeld: `(1, One)` is een `(Int, Result)` expressie.

Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.

## <a name="user-defined-type-expressions"></a>Door de gebruiker gedefinieerde type expressies

Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.
Als `IntPair` bijvoorbeeld een door de gebruiker gedefinieerd type is op basis van `(Int, Int)`, `IntPair(2,3)` is dit een geldige letterlijke waarde van dat type.

Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.

## <a name="unwrap-expressions"></a>Onverpakte expressies

In Q # is de operator voor uitpakken een afsluitend uitroep `!`teken.
Zo `IntPair` is bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend `(Int, Int)`type `s` en was dit een variabele `IntPair(2,3)`met de `s!` waarde. `(2,3)`vervolgens zou het zijn.

Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen. de operator voor uitpakken kan worden herhaald. `s!!` Hiermee geeft u bijvoorbeeld de dubbele waarde onverpakt van `s`op.
Als `WrappedPair` is dus een door de gebruiker gedefinieerd type met een onderliggend `IntPair`type en `t` dit is een `WrappedPair(IntPair(1,2))`variabele met `t!!` de waarde `(1,2)`, dan zou.

De `!` operator heeft een hogere prioriteit dan alle andere opera tors `[]` dan voor het indexeren van matrices en het segmenteren.
`!`en `[]` positioneel binden; dat wil zeggen `a[i]![3]` `((a[i])!)[3]`: Neem het element van de `i`' th ' in `a`, pak het uit en haal vervolgens het derde element van de niet-ingepakte waarde op (dit moet een matrix zijn).

De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.
Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.
Bijvoorbeeld:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Matrix expressies

Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen `[` en. `]`
Alle elementen moeten compatibel zijn met hetzelfde type.

Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.
Het element type van de matrix ondersteunt alle functors die door alle elementen worden ondersteund.
`Op1`Bijvoorbeeld als `Op2`,, en `Op3` alle zijn `Qubit[] => Unit`, maar `Op1` ondersteunt `Adjoint`, `Op2` ondersteunt `Controlled`en `Op3` ondersteunt:

- `[Op1, Op2]`is een matrix met `(Qubit[] => Unit)` bewerkingen.
- `[Op1, Op3]`is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.
- `[Op2, Op3]`is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.

Lege letterlijke arrays `[]`,, zijn niet toegestaan.
In plaats `new ★[0]`daarvan kunt `★` u, waar als tijdelijke aanduiding voor een geschikt type, de gewenste matrix met een lengte van nul maken.

Als er twee matrices van hetzelfde type zijn opgegeven, kan `+` de binaire operator worden gebruikt voor het vormen van een nieuwe matrix die de samen voeging van de twee matrices vormt.
`[1,2,3] + [4,5,6]` Bijvoorbeeld: `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Matrix maken

Op basis van een type `Int` en een expressie `new` kan de operator worden gebruikt voor het toewijzen van een nieuwe matrix met de opgegeven grootte.
Bijvoorbeeld, zou `new Int[i+1]` een nieuwe `Int` matrix met `i+1` elementen kunnen toewijzen.

De elementen van een nieuwe matrix worden geïnitialiseerd op een type-afhankelijke standaard waarde.
In de meeste gevallen is dit een bepaalde variatie van nul.

Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.
Daarom is de standaard waarde voor deze typen een ongeldige verwijzing die niet kan worden gebruikt zonder dat er een runtime-fout wordt veroorzaakt.
Dit is vergelijkbaar met een null-verwijzing in talen als C# of Java.
Matrices met qubits of callables moeten correct worden geïnitialiseerd met niet-standaard waarden voordat de elementen veilig kunnen worden gebruikt. Geschikte initialisatie routines kunt u vinden in <xref:microsoft.quantum.arrays>.

De standaard waarden voor elk type zijn:

Type | Standaard
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | _Ongeldige Qubit_
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | Het lege bereik,`1..1..0`
 `Callable` | _Ongeldige aanroepable_
 `Array['T]` | `'T[0]`

De tuple-typen zijn geïnitialiseerd met element-by-element.


### <a name="jagged-arrays"></a>Gekartelde matrices

Een gekartelde matrix, ook wel een matrix van matrices genoemd, is een matrix waarvan de elementen matrices zijn. De elementen van een gekartelde matrix kunnen van verschillende grootten zijn. In het volgende voor beeld ziet u hoe u een gekartelde matrix die een vermenigvuldigings tabel vertegenwoordigt, declareert en initialiseert.

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {

    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```


### <a name="array-slices"></a>Matrix segmenten

Met een matrix expressie en een `Range` expressie kan een nieuwe expressie worden gevormd met behulp `[` van `]` de operator en de matrix segment.
De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die worden geïndexeerd door de elementen van de `Range`, in de volg orde die is `Range`gedefinieerd door de.
`a` Als `Double`bijvoorbeeld is gebonden aan een matrix van s, `a[3..-1..0]` is dit een `Double[]` expressie die de eerste vier elementen van `a` , maar in de omgekeerde volg orde bevat zoals ze worden weer `a`gegeven in.

Als het `Range` leeg is, is het resulterende matrix segment nul lengte.

Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om te kunnen worden gesegmenteerd.
Als `a` bijvoorbeeld beide matrices van `b` `Int`s zijn, wordt een segment uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[1..2..7]
```

Alle matrices in Q # zijn gebaseerd op nul.
Dat wil zeggen, het eerste element van een `a` matrix is `a[0]`altijd.

Vanaf onze 0,8-release ondersteunen we context afhankelijke expressies voor bereik segmenting. Met name bereik begin-en eind waarden kunnen worden wegge laten in de context van een expressie voor bereik segmentering. In dat geval past de compiler de volgende regels toe om de beoogde scheidings tekens voor het bereik af te leiden. 

Als de begin waarde van het bereik bijvoorbeeld wordt wegge laten, wordt de uitgestelde begin waarde 
- is nul als er geen stap is opgegeven of als de opgegeven stap positief is en 
- is de lengte van de gesegmenteerde matrix min één als de opgegeven stap negatief is. 

Als de eind waarde van het bereik wordt wegge laten, wordt de uitgestelde eind waarde 
- is de lengte van de gesegmenteerde matrix min één als er geen stap is opgegeven, of als de opgegeven stap positief is en 
- is nul als de opgegeven stap negatief is. 

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

## <a name="array-element-expressions"></a>Matrix element expressies

Met een matrix expressie en een `Int` expressie kan een nieuwe expressie worden gevormd met de operator `[` and `]` van het matrix element.
De nieuwe expressie is van hetzelfde type als het element type van de matrix.
Als `a` bijvoorbeeld is gebonden aan een matrix van `Double`s, dan `a[4]` is een `Double` expressie.

Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om een element te selecteren.
Als `a` bijvoorbeeld beide matrices van `b` `Int`s zijn, wordt een element uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[13]
```

Alle matrices in Q # zijn gebaseerd op nul.
Dat wil zeggen, het eerste element van een `a` matrix is `a[0]`altijd.


## <a name="copy-and-update-expressions"></a>Expressies kopiëren en bijwerken

Nieuwe matrices kunnen worden gemaakt op basis van bestaande met behulp van Copy-en-update-expressies.
Een copy-en-update-expressie is een expressie van het `expression1 w/ expression2 <- expression3`formulier, `expression1` waarbij type `T[]` voor een type `T`is. De tweede `expression2` definieert de indices van de element (en) die moeten worden gewijzigd vergeleken met de matrix `expression1` in en moet van het type `Int` of van het type `Range`zijn. Als `expression2` is van het `Int`type `expression3` , moet van het type `T`zijn. Als `expression2` is van het `Range`type `expression3` , moet van het type `T[]`zijn.

Met een copy-and-update `arr w/ idx <- value` -expressie wordt een nieuwe matrix gemaakt met alle elementen die zijn ingesteld op `arr`het overeenkomstige element in, met uitzonde ring `idx`van het element (en) op, die zijn ingesteld `value`op een of meer in. Als `arr` bijvoorbeeld een matrix `[0,1,2,3]`bevat, 
- `arr w/ 0 <- 10`is de matrix `[10,1,2,3]`.
- `arr w/ 2 <- 10`is de matrix `[0,1,10,3]`.
- `arr w/ 0..2..3 <- [10,12]`is de matrix `[10,1,12,3]`.

Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen. Denk bijvoorbeeld aan het type 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Als `c` de waarde van het type `Complex(1.,-1.)`bevat, `c w/ Re <- 0.` is dit een expressie van `Complex` het type waarmee wordt `Complex(0.,-1.)`geëvalueerd.

## <a name="conditional-expressions"></a>Voorwaardelijke expressies

Als er twee andere expressies van hetzelfde type en een booleaanse expressie zijn opgegeven, kan de voorwaardelijke expressie worden gevormd met behulp van het `?` vraag `|`teken en de verticale balk.
Bijvoorbeeld `a==b ? c | d`.
In dit voor beeld is de waarde van de voorwaardelijke expressie `c` als `a==b` True en `d` als deze False is.

De twee expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.
In dit geval is het type van de voorwaardelijke expressie een bewerking met de invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.
`Op1`Bijvoorbeeld als `Op2`,, en `Op3` alle zijn `Qubit[]=>Unit`, maar `Op1` ondersteunt `Adjoint`, `Op2` ondersteunt `Controlled`en `Op3` ondersteunt:

- `flag ? Op1 | Op2`is een `(Qubit[] => Unit)` bewerking.
- `flag ? Op1 | Op3`is een `(Qubit[] => Unit is Adj)` bewerking.
- `flag ? Op2 | Op3`is een `(Qubit[] => Unit is Ctl)` bewerking.

Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in het resultaat dat de waarde van de aanroep zal zijn.
Als `a==b ? C(qs) | D(qs)` `a==b` bijvoorbeeld is ingesteld op True, wordt de `C` bewerking opgeroepen en als deze ONWAAR is, wordt alleen `D` aangeroepen.
Dit is vergelijkbaar met kort circuits in andere talen.


## <a name="operator-precedence"></a>Operator prioriteit

Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde `^`ring van.

U kunt voor `[` elke `]`operator een binding maken, en voor het segmenteren en indexeren van matrices.

De functors `Adjoint` en `Controlled` binding na het indexeren van de matrix, maar vóór alle andere opera tors.

Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.

Opera tors in volg orde van prioriteit, van hoog naar laag:

Operator | Ariteit | Beschrijving | Typen operand
---------|----------|---------|---------------
 Volg`!` | Unaire | Uitpakken | Een door de gebruiker gedefinieerd type
 `-`, `~~~`, `not` | Unaire | Numerieke, negatieve, bitsgewijze complement, logische negatie | `Int`, `BigInt` of `Double` `-`voor, `Int` of `BigInt` voor `~~~`, `Bool` voor`not`
 `^` | Binair | Geheel getal energie | `Int`of `BigInt` voor de basis `Int` voor de exponent
 `/`, `*`, `%` | Binair | Deling, vermenigvuldiging, integer modulus | `Int`, `BigInt` of `Double` voor `/` en `*`, `Int` of `BigInt` voor`%`
 `+`, `-` | Binair | Toevoeging of teken reeks-en matrix samenvoeging, aftrekken | `Int`, `BigInt` of `Double`, ook `String` of een matrix type voor`+`
 `<<<`, `>>>` | Binair | Shift-links, Shift-rechts | `Int` of `BigInt`
 `<`, `<=`, `>`, `>=` | Binair | Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen | `Int`, `BigInt` of`Double`
 `==`, `!=` | Binair | gelijk, niet-gelijk-vergelijkingen | een primitief type
 `&&&` | Binair | Bitsgewijze AND | `Int` of `BigInt`
 `^^^` | Binair | Bitsgewijze XOR | `Int` of `BigInt`
 <code>\|\|\|</code> | Binair | Bitsgewijze OR | `Int` of `BigInt`
 `and` | Binair | Logische en | `Bool`
 `or` | Binair | Logische of | `Bool`
 `..` | Binair/Ternair | De operator Range | `Int`
 `?` `|` | Ternair | Voorwaardelijk | `Bool`voor de linkerkant
`w/` `<-` | Ternair | Kopiëren en bijwerken | Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)
