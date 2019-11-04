---
title: Expressies | Microsoft Docs
description: Expressies
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 09d493df4e1178fee1f7a5946cfda2f411111006
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185202"
---
# <a name="expressions"></a>Expressies

## <a name="grouping"></a>Shapes

Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.
`(7)` is bijvoorbeeld een `Int` expressie, `([1,2,3])` een expressie van het type matrix van `Int`s en `((1,2))` is een expressie van het type `(Int, Int)`.

De equivalentie tussen eenvoudige waarden en enkele Tuples die in [het type model](xref:microsoft.quantum.language.type-model#tuple-types) worden beschreven, verwijdert de dubbel zinnigheid tussen `(6)` als een groep en `(6)` als een tuple met één element.

## <a name="symbols"></a>Mogen

De naam van een symbool dat is gekoppeld aan of is toegewezen aan een waarde van het type `'T` is een expressie van het type `'T`.
Als het symbool `count` bijvoorbeeld is gebonden aan de gehele waarde `5`, is `count` een expressie voor gehele getallen.

## <a name="numeric-expressions"></a>Numerieke expressies

Numerieke expressies zijn expressies van het type `Int`, `BigInt`of `Double`.
Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.

`Int` letterlijke waarden in Q # zijn identiek aan letterlijke waarden C#in het geheel getal in, behalve dat er geen ' l ' of ' l ' vereist is (of toegestaan).
Hexadecimale en binaire gehele getallen worden respectievelijk met het voor voegsel ' 0x ' en ' 0b ' ondersteund.

`BigInt` letterlijke waarden in Q # zijn gelijk aan teken reeksen met een groot geheel getal in .NET, met een afsluitende "l" of "L".
Hexadecimale Big-gehele getallen worden ondersteund met het voor voegsel 0x.
Daarom zijn de volgende geldige toepassingen van `BigInt` literals:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double` letterlijke waarden in Q # zijn identiek aan dubbele letterlijke C#waarden in, behalve dat er geen ' d ' of ' d ' vereist is (of toegestaan).

Gezien een matrix expressie van elk element type, kan een `Int`-expressie worden gevormd met behulp van de ingebouwde functie `Length`, waarbij de matrix expressie tussen haakjes, `(` en `)`is opgenomen.
Als `a` bijvoorbeeld is gebonden aan een matrix, wordt `Length(a)` een expressie voor gehele getallen.
Als `b` een matrix is met gehele getallen, `Int[][]`en vervolgens `Length(b)` het aantal submatrixen in `b`en `Length(b[1])` het aantal gehele getallen in de tweede submatrix in `b`.

Als u twee numerieke expressies van hetzelfde type hebt opgegeven, kunnen de binaire Opera tors `+`, `-`, `*`en `/` worden gebruikt om een nieuwe numerieke expressie te vormen.
Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.

Als u twee geheeltallige expressies hebt opgegeven, kan de binaire operator `^` (Power) worden gebruikt om een nieuwe expressie met gehele getallen te vormen.
Op dezelfde manier kan `^` worden gebruikt met twee dubbele expressies om een nieuwe dubbele expressie te vormen.
Ten slotte kan `^` worden gebruikt met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant om een nieuwe Big Integer-expressie te vormen.
In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.

Als er twee integere of Big Integer-expressies zijn opgegeven, kan een nieuwe integer of Big Integer-expressie worden gevormd met behulp van de `%` (modulus), `&&&` (bitsgewijze AND), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR)-opera tors.

Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de rechter kant, de `<<<` (reken kundige verschuiving links) of `>>>` (reken kundige rechter verschuiving) opera tors kunnen worden gebruikt voor het maken van een nieuwe expressie met hetzelfde type als de linkerhand expressie.

De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.
Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.
Als het getal dat moet worden verplaatst een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64`; dat wil zeggen dat een verschuiving van 1 en een verschuiving van 65 hetzelfde effect hebben.

Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.
Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.
Dat wil zeggen dat de ene stap naar links of rechts verschuift precies hetzelfde is als vermenigvuldigen of delen met 2.

Geheel getal en een absolute modulus volgen hetzelfde gedrag voor negatieve getallen als C#.
Dat wil zeggen dat `a % b` altijd hetzelfde teken als `a`heeft en `b * (a / b) + a % b` altijd gelijk is aan `a`.
Bijvoorbeeld:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Het delen van een groot geheel getal en modulus werkt op dezelfde manier.

Op basis van een numerieke expressie kan een nieuwe expressie worden gevormd met behulp van de `-` unaire operator.
De nieuwe expressie is van hetzelfde type als de component-expressie.

Als een geheel getal of een Big Integer-expressie is opgegeven, kan een nieuwe expressie van hetzelfde type worden gevormd met behulp van de `~~~` (bitsgewijze complement) monadische operator.

## <a name="boolean-expressions"></a>Booleaanse expressies

De twee `Bool` letterlijke waarden zijn `true` en `false`.

Als u twee expressies van hetzelfde primitieve type hebt opgegeven, kunnen de binaire Opera tors `==` en `!=` worden gebruikt om een `Bool` expressie te maken.
De expressie is waar als de twee expressies (niet) gelijk zijn.

Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken, alleen de waarden ervan kunnen worden vergeleken. Bijvoorbeeld:

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Gelijkheids vergelijking voor `Qubit` waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.
De status van de twee qubits wordt niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.

Gelijkheids vergelijking voor `Double` waarden kan misleiden door Afrondings effecten.
Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.

Met een wille keurige combi natie van twee numerieke expressies kunnen de binaire Opera tors `>`, `<`, `>=`en `<=` worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan of kleiner dan of gelijk aan de tweede expressie.

Op basis van twee Booleaanse expressies kunnen de binaire Opera tors `and` en `or` worden gebruikt voor het maken van een nieuwe Boole-expressie die waar is als beide expressies beide zijn ingesteld op True.

Met een booleaanse expressie kan de `not` unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.

## <a name="string-expressions"></a>Teken reeks expressies

Q # Hiermee kunnen teken reeksen worden gebruikt in de `fail`-instructie en de `Log`-standaard functie.

Teken reeksen in Q # zijn letterlijke waarden of geïnterpoleerde teken reeksen.
Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks Unicode-tekens tussen dubbele aanhalings `"`.
In een teken reeks kan de back slash `\` worden gebruikt om een dubbel aanhalings teken te escapen en om een nieuwe regel in te voegen als `\n`, een regel terugloop als `\r`en een tab als `\t`.
Bijvoorbeeld:

```qsharp
"\"Hello world!\", she said.\n"
```

De syntaxis van Q # voor teken reeks-interpolatie is een subset C# van de 7,0-syntaxis. Q # biedt geen ondersteuning voor Verbatim-geïnterpoleerde teken reeksen (meerdere regels).
Zie [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) voor C# de syntaxis.

Expressies binnen een geïnterpoleerde teken reeks volgen Q # syntaxis, geen C# syntaxis.
Een geldige Q #-expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.

## <a name="qubit-expressions"></a>Qubit-expressies

De enige `Qubit`-expressies zijn symbolen die zijn gekoppeld aan `Qubit` waarden of matrix elementen van `Qubit` matrices.
Er zijn geen `Qubit` letterlijke waarden.

## <a name="pauli-expressions"></a>Pauli-expressies

De vier `Pauli` waarden, `PauliI`, `PauliX`, `PauliY`en `PauliZ`, zijn alle geldige `Pauli` expressies.

Behalve dat zijn de enige `Pauli`-expressies symbolen die zijn gekoppeld aan `Pauli` waarden of matrix elementen van `Pauli` matrices.

## <a name="result-expressions"></a>Resultaat expressies

De twee `Result` waarden, `One` en `Zero`, zijn geldige `Result` expressies.

Behalve dat zijn de enige `Result`-expressies symbolen die zijn gekoppeld aan `Result` waarden of matrix elementen van `Result` matrices.
Houd er met name rekening mee dat `One` niet hetzelfde is als de gehele `1`en dat er geen rechtstreekse conversie tussen deze waarden is.
Dit geldt ook voor `Zero` en `0`.

## <a name="range-expressions"></a>Bereik expressies

Als er drie `Int` expressies `start`, `step`en `stop`, is `start .. step .. stop` een bereik expressie waarvan het eerste element is `start`, het tweede element is `start+step`, het derde element is `start+step+step`, enzovoort, totdat `stop` wordt door gegeven.
Een bereik kan leeg zijn als `step` bijvoorbeeld positief is en `stop < start`.
Het laatste element van het bereik wordt `stop` als het verschil tussen `start` en `stop` een integraal veelvoud van `step`is; dat wil zeggen dat het bereik op beide uiteinden is inbegrepen.

Op basis van twee `Int` expressies `start` en `stop`is `start .. stop` een bereik expressie die gelijk is aan `start .. 1 .. stop`.
Houd er rekening mee dat de geïmpliceerde `step` + 1, zelfs als `stop` kleiner is dan `start`. in dat geval is het bereik leeg.

Enkele voor beelden van bereiken:

- `1..3` is het bereik van 1, 2, 3.
- `2..2..5` is het bereik van 2, 4.
- `2..2..6` is het bereik 2, 4, 6.
- `6..-2..2` is het bereik van 6, 4, 2.
- `2..1` is een leeg bereik.
- `2..6..7` is het bereik 2.
- `2..2..1` is een leeg bereik.
- `1..-1..2` is een leeg bereik.

## <a name="callable-expressions"></a>Aanroep bare expressies

Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.
`X` is bijvoorbeeld een letterlijke bewerkings bewerking die verwijst naar de standaard bibliotheek `X` bewerking en `Message` een letterlijke functie is die verwijst naar de functie standaard bibliotheek `Message`.

Als een bewerking de `Adjoint` functor ondersteunt, is `Adjoint op` een bewerkings expressie.
En als de bewerking de `Controlled` functor ondersteunt, is `Controlled op` een bewerkings expressie.
De typen van deze expressies worden opgegeven in [functors](xref:microsoft.quantum.language.type-model#functors).

Functors (`Adjoint` en `Controlled`) zijn beter te binden dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met `[]`.
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

Als `Fun` bijvoorbeeld een functie met hand tekening `'T1->Unit`:

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aanroep bare aanroepende expressies

Gezien een aanroep bare (Operation-of Function-) expressie en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kan een aanroep expressie worden gevormd door de tuple-expressie toe te voegen aan de aanroep bare expressie.
Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.

Als `Op` bijvoorbeeld een bewerking met een handtekening `((Int, Qubit) => Double)`is, is `Op(3, qubit1)` een expressie van het type `Double`.
Als `Sin` een functie met hand tekening `(Double -> Double)`is, is `Sin(0.1)` een expressie van het type `Double`.
Ten slotte, als `Builder` een functie met hand tekening `(Int -> (Int -> Int))`is, is `Builder(3)` een functie van tot int.

Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.
Als u het resultaat van het aanroepen van `Builder` vanuit de vorige alinea wilt aanroepen, is de juiste syntaxis:

```qsharp
(Builder(3))(2)
```

Bij het aanroepen van een aanroep bare type para meter kunnen de werkelijke type parameters worden opgegeven tussen punt haken `<` en `>` na de aanroep bare expressie.
Dit is doorgaans onnodig omdat de compiler Q # de daad werkelijke typen afleidt.
Het is vereist voor een gedeeltelijke toepassing (zie hieronder) als een argument van het type para meters niet-opgegeven is.
Het is ook soms handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.

Als `Func` hand tekening heeft `('T1, 'T2, 'T1) -> 'T2`, `Op1` en `Op2` hand tekening `(Qubit[] => Unit is Adj)`heeft en `Op3` hand tekening heeft `(Qubit[] => Unit)`, om `Func` met `Op1` als eerste argument te openen, `Op2` als de tweede en `Op3` als derde:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

De type specificatie is vereist omdat `Op3` en `Op1` verschillende typen hebben, zodat de compiler dit als dubbel zinnig behandelt zonder de specificatie.

### <a name="partial-application"></a>Gedeeltelijke toepassing

Op basis van een aanroep bare expressie kan een nieuwe aanroep worden gemaakt door een subset van de argumenten op te geven die kunnen worden aangeroepen.
Dit wordt _gedeeltelijke toepassing_genoemd.

In Q # wordt een gedeeltelijk toegepaste aanroepable weer gegeven door een expressie met een gewone aanroep te schrijven, maar met een onderstrepings teken, `_`voor de niet-opgegeven argumenten.
De resulterende aanroepable heeft hetzelfde resultaat type als het basis aanroepable en dezelfde specialisatie voor bewerkingen.
Het invoer type van de gedeeltelijke toepassing is gewoon het oorspronkelijke type met de opgegeven argumenten verwijderd.

Als een onveranderlijke variabele wordt door gegeven als een opgegeven argument bij het maken van een gedeeltelijke toepassing, wordt de huidige waarde van de variabele gebruikt.
Als u de waarde van de variabele achteraf wijzigt, heeft dit geen invloed op de gedeeltelijke toepassing.

Als `Op` bijvoorbeeld het type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`heeft:

- `Op(5,(_,_))` is van het type `(((Qubit,Qubit), Double) => Unit is Adj)`en is `Op(5,_)`.
- `Op(_,(_,1.0))` is van het type `((Int, (Qubit,Qubit)) => Unit is Adj)`.
- `Op(_,((q1,q2),_))` is van het type `((Int,Double) => Unit is Adj)`.
   Let op: we hebben hier Singleton-tuple-equivalentie toegepast.

Als het gedeeltelijk toegepaste aanroep type para meters heeft die niet kunnen worden afgeleid door de compiler, moeten deze worden opgegeven op de aanroep site.
De gedeeltelijke toepassing mag geen niet-opgegeven type parameters hebben.

Als `Op` bijvoorbeeld het type `(('T1, Qubit, 'T1) => Unit : Adjoint)`heeft:

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

Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen `(` en `)`.
`(1, One)` is bijvoorbeeld een `(Int, Result)`-expressie.

Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.

## <a name="user-defined-type-expressions"></a>Door de gebruiker gedefinieerde type expressies

Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.
Als `IntPair` bijvoorbeeld een door de gebruiker gedefinieerd type op basis van `(Int, Int)`is, dan is `IntPair(2,3)` een geldige letterlijke waarde van dat type.

Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.

## <a name="unwrap-expressions"></a>Onverpakte expressies

In Q # is de operator voor uitpakken een afsluitend uitroep teken `!`.
Als `IntPair` bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `(Int, Int)`is en `s` een variabele met de waarde `IntPair(2,3)`, dan zou `s!` worden `(2,3)`.

Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen. de operator voor uitpakken kan worden herhaald. `s!!` geeft bijvoorbeeld de dubbele waarde onverpakt op `s`.
Als `WrappedPair` bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `IntPair`en `t` een variabele met de waarde `WrappedPair(IntPair(1,2))`, dan zou `t!!` worden `(1,2)`.

De operator `!` heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.
`!` en `[]` positioneel binden; dat wil zeggen dat `a[i]![3]` moet worden gelezen als `((a[i])!)[3]`: Neem het element van de `i`van `a`, pak het uit en haal vervolgens het derde element van de niet-ingepakte waarde op (dit moet een matrix zijn).

De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.
Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.
Bijvoorbeeld:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Matrix expressies

Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen `[` en `]`.
Alle elementen moeten compatibel zijn met hetzelfde type.

Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.
Het element type van de matrix ondersteunt alle functors die door alle elementen worden ondersteund.
Als `Op1`, `Op2`en `Op3` allemaal `Qubit[] => Unit`zijn, maar `Op1` ondersteuning biedt voor `Adjoint`, `Op2` ondersteunt `Controlled`, en `Op3` beide ondersteunen:

- `[Op1, Op2]` is een matrix met `(Qubit[] => Unit)` bewerkingen.
- `[Op1, Op3]` is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.
- `[Op2, Op3]` is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.

Lege letterlijke arrays, `[]`, zijn niet toegestaan.
In plaats daarvan gebruikt u `new ★[0]`, waarbij `★` als tijdelijke aanduiding voor een geschikt type is, de gewenste matrix met een lengte van nul kunt maken.

Als er twee matrices van hetzelfde type zijn opgegeven, kan de operator binary `+` worden gebruikt voor het vormen van een nieuwe matrix die de samen voeging van de twee matrices vormt.
`[1,2,3] + [4,5,6]` is bijvoorbeeld `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Matrix maken

Op basis van een type en een `Int`-expressie kan de operator `new` worden gebruikt voor het toewijzen van een nieuwe matrix met de opgegeven grootte.
`new Int[i+1]` zou bijvoorbeeld een nieuwe `Int` matrix met `i+1` elementen toewijzen.

De elementen van een nieuwe matrix worden geïnitialiseerd op een type-afhankelijke standaard waarde.
In de meeste gevallen is dit een bepaalde variatie van nul.

Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.
Daarom is de standaard waarde voor deze typen een ongeldige verwijzing die niet kan worden gebruikt zonder dat er een runtime-fout wordt veroorzaakt.
Dit is vergelijkbaar met een null-verwijzing in talen zoals C# of Java.
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
 `Range` | Het lege bereik `1..1..0`
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

Op basis van een matrix expressie en een `Range` expressie kan een nieuwe expressie worden gevormd met de segment operator `[` en `]` matrix.
De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die worden geïndexeerd door de elementen van de `Range`, in de volg orde die wordt gedefinieerd door de `Range`.
Als `a` bijvoorbeeld is gebonden aan een matrix van `Double`s, is `a[3..-1..0]` een `Double[]`-expressie die de eerste vier elementen van `a` bevat, maar in de omgekeerde volg orde zoals ze in `a`worden weer gegeven.

Als de `Range` leeg is, krijgt het resulterende matrix segment de lengte nul.

Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om te kunnen worden gesegmenteerd.
Als `a` en `b` beide matrices van `Int`s zijn, wordt een segment uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[1..2..7]
```

Alle matrices in Q # zijn gebaseerd op nul.
Dat wil zeggen dat het eerste element van een matrix `a` altijd `a[0]`is.

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

Op basis van een matrix expressie en een `Int`-expressie kan een nieuwe expressie worden gevormd met de operator `[` en `]` matrix element.
De nieuwe expressie is van hetzelfde type als het element type van de matrix.
Als `a` bijvoorbeeld is gebonden aan een matrix van `Double`s, is `a[4]` een `Double`-expressie.

Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om een element te selecteren.
Als bijvoorbeeld `a` en `b` beide matrices van `Int`s zijn, wordt een element uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[13]
```

Alle matrices in Q # zijn gebaseerd op nul.
Dat wil zeggen dat het eerste element van een matrix `a` altijd `a[0]`is.


## <a name="copy-and-update-expressions"></a>Expressies kopiëren en bijwerken

Nieuwe matrices kunnen worden gemaakt op basis van bestaande met behulp van Copy-en-update-expressies.
Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3`, waarbij `expression1` van het type `T[]` moet zijn voor bepaalde typen `T`. De tweede `expression2` definieert de indices van de element (en) die moeten worden gewijzigd vergeleken met de matrix in `expression1` en moet een type `Int` of van het type `Range`zijn. Als `expression2` van het type `Int`is, moet `expression3` van het type `T`zijn. Als `expression2` van het type `Range`is, moet `expression3` van het type `T[]`zijn.

Met een copy-and-update-expressie `arr w/ idx <- value` wordt een nieuwe matrix gemaakt met alle elementen die zijn ingesteld op het overeenkomstige element in `arr`, met uitzonde ring van het element (en) op `idx`, die zijn ingesteld op een of meer in `value`. Als `arr` bijvoorbeeld een matrix `[0,1,2,3]`bevat, 
- `arr w/ 0 <- 10` is de matrix `[10,1,2,3]`.
- `arr w/ 2 <- 10` is de matrix `[0,1,10,3]`.
- `arr w/ 0..2..3 <- [10,12]` is de matrix `[10,1,12,3]`.

Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen. Denk bijvoorbeeld aan het type 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Als `c` de waarde van het type `Complex(1.,-1.)`bevat, is `c w/ Re <- 0.` een expressie van het type `Complex` die als `Complex(0.,-1.)`wordt geëvalueerd.

## <a name="conditional-expressions"></a>Voorwaardelijke expressies

Als er twee andere expressies van hetzelfde type en een booleaanse expressie worden opgegeven, kan de voorwaardelijke expressie worden gevormd met behulp van het vraag teken `?` en de verticale balk `|`.
Bijvoorbeeld `a==b ? c | d`.
In dit voor beeld wordt de waarde van de voorwaardelijke expressie `c` als `a==b` waar is en `d` als deze is ingesteld op false.

De twee expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.
In dit geval is het type van de voorwaardelijke expressie een bewerking met de invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.
Als `Op1`, `Op2`en `Op3` allemaal `Qubit[]=>Unit`zijn, maar `Op1` ondersteuning biedt voor `Adjoint`, `Op2` ondersteunt `Controlled`, en `Op3` beide ondersteunen:

- `flag ? Op1 | Op2` is een `(Qubit[] => Unit)` bewerking.
- `flag ? Op1 | Op3` is een `(Qubit[] => Unit is Adj)` bewerking.
- `flag ? Op2 | Op3` is een `(Qubit[] => Unit is Ctl)` bewerking.

Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in het resultaat dat de waarde van de aanroep zal zijn.
Als `a==b` bijvoorbeeld is ingesteld `a==b ? C(qs) | D(qs)`op True, wordt de `C`-bewerking aangeroepen en als deze ONWAAR is, wordt alleen `D` aangeroepen.
Dit is vergelijkbaar met kort circuits in andere talen.


## <a name="operator-precedence"></a>Operator prioriteit

Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^`.

De vier Kante haken, `[` en `]`, voor het segmenteren en indexeren van matrices, bind vóór een operator.

De functors-`Adjoint` en `Controlled` BIND na het indexeren van de matrix, maar vóór alle andere opera tors.

Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.

Opera tors in volg orde van prioriteit, van hoog naar laag:

Operator | Ariteit | Beschrijving | Typen operand
---------|----------|---------|---------------
 afsluitende `!` | Monadische | Uitpakken | Een door de gebruiker gedefinieerd type
 `-`, `~~~`, `not` | Monadische | Numerieke, negatieve, bitsgewijze complement, logische negatie | `Int`, `BigInt` of `Double` voor `-`, `Int` of `BigInt` voor `~~~`, `Bool` voor `not`
 `^` | waarde | Geheel getal energie | `Int` of `BigInt` voor de basis, `Int` voor de exponent
 `/`, `*`, `%` | waarde | Deling, vermenigvuldiging, integer modulus | `Int`, `BigInt` of `Double` voor `/` en `*`, `Int` of `BigInt` voor `%`
 `+`, `-` | waarde | Toevoeging of teken reeks-en matrix samenvoeging, aftrekken | `Int`, `BigInt` of `Double`, ook `String` of een wille keurig type matrix voor `+`
 `<<<`, `>>>` | waarde | Shift-links, Shift-rechts | `Int` of `BigInt`
 `<`, `<=`, `>`, `>=` | waarde | Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen | `Int`, `BigInt` of `Double`
 `==`, `!=` | waarde | gelijk, niet-gelijk-vergelijkingen | een primitief type
 `&&&` | waarde | Bitsgewijze AND | `Int` of `BigInt`
 `^^^` | waarde | Bitsgewijze XOR | `Int` of `BigInt`
 <code>\|\|\|</code> | waarde | Bitsgewijze OR | `Int` of `BigInt`
 `and` | waarde | Logische en | `Bool`
 `or` | waarde | Logische of | `Bool`
 `..` | Binair/Ternair | De operator Range | `Int`
 `?` `|` | Ternair | Voorwaardelijk | `Bool` voor de linkerkant
`w/` `<-` | Ternair | Kopiëren en bijwerken | Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)
