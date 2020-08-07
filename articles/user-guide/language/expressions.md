---
title: Expressies inQ#
description: Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q# .
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- Q#
- $$v
ms.openlocfilehash: b6cc97dfee05dc843e213e84f17043714a8a9656
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869610"
---
# <a name="expressions-in-no-locq"></a>Expressies inQ#

## <a name="numeric-expressions"></a>Numerieke expressies

Numerieke expressies zijn expressies van het type `Int` , `BigInt` of `Double` .
Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.

`Int`letterlijke waarden in Q# worden geschreven als een reeks cijfers.
Hexadecimale en binaire gehele getallen worden ondersteund en worden met `0x` respectievelijk een en `0b` -voor voegsel geschreven.

`BigInt`letterlijke waarden in Q# hebben een navolgende `l` of `L` achtervoegsel.
Hexadecimale Big gehele getallen worden ondersteund en geschreven met het voor voegsel ' 0x '.
Daarom zijn de volgende geldige toepassingen van `BigInt` letterlijke waarden:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`letterlijke waarden in Q# zijn drijvende-komma getallen die zijn geschreven met decimale cijfers.
Ze kunnen worden geschreven met of zonder een decimaal teken, `.` of een exponentieel onderdeel dat is aangegeven met e of e (waarna alleen een mogelijk minteken en decimaal tekens geldig zijn).
Hier volgen geldige `Double` letterlijke waarden: `0.0` , `1.2e5` , `1e-5` .

Op basis van een matrix expressie van elk element type kunt u een `Int` expressie maken met behulp van de [`Length`](xref:microsoft.quantum.core.length) ingebouwde functie, waarbij de matrix expressie tussen haakjes staat.
Als bijvoorbeeld `a` is gebonden aan een matrix, `Length(a)` is dit een expressie met gehele getallen.
Als `b` is een matrix met matrices van gehele getallen, `Int[][]` `Length(b)` is dit het aantal submatrixen in `b` en `Length(b[1])` is het aantal gehele getallen in de tweede submatrix in `b` .

Gegeven twee numerieke expressies van hetzelfde type, de binaire Opera tors `+` , `-` , `*` en `/` kunnen worden gebruikt om een nieuwe numerieke expressie te vormen.
Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.

Als u twee geheeltallige expressies hebt opgegeven, gebruikt u de binaire operator `^` (Power) om een nieuwe expressie met gehele getallen te vormen.
U kunt ook `^` met twee dubbele expressies gebruiken om een nieuwe dubbele expressie te maken.
Ten slotte kunt u `^` met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant gebruiken om een nieuwe Big Integer-expressie te vormen.
In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.

Als er twee integere of Big Integer-expressies zijn, moet u een nieuwe geheel getal of Big Integer-expressie vormen met behulp van de `%` Opera tors (modulus), `&&&` (bitsgewijze en), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR).

Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de rechter kant, gebruik de `<<<` (reken kundige verschuiving links) of `>>>` (reken kundige Shift-rechts) om een nieuwe expressie te maken met hetzelfde type als de linker expressie.

De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.
Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.
Als het getal verschuiven een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64` ; dat wil zeggen, een verschuiving van 1 en een verschuiving van 65 hebben hetzelfde effect.

Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.
Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.
Dat wil zeggen dat de ene stap naar links of rechts verschuift, hetzelfde is als vermenigvuldigen of delen met 2.

Geheel getal delen en integers modulus volgen hetzelfde gedrag voor negatieve getallen als C#.
Dat wil zeggen, `a % b` heeft altijd hetzelfde teken als `a` en is `b * (a / b) + a % b` altijd gelijk aan `a` .
Bijvoorbeeld:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 5 | 2 | -2 | -1
 5 | -2 | 2 | -1

Groot geheel getal delen en modulus bewerkingen werken op dezelfde manier.

Met een wille keurige numerieke expressie kunt u een nieuwe expressie maken met behulp van de `-` unaire operator.
De nieuwe expressie is van hetzelfde type als de onderdeel expressie.

Als een geheel getal of een Big Integer-expressie, kunt u een nieuwe expressie van hetzelfde type vormen met behulp van de `~~~` (bitsgewijze complement) monadische operator.

## <a name="boolean-expressions"></a>Booleaanse expressies

De twee `Bool` letterlijke waarden zijn `true` en `false` .

Op basis van twee expressies van hetzelfde primitieve type `==` kunnen de en `!=` binaire Opera tors worden gebruikt voor het maken van een `Bool` expressie.
De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.

Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken. Als u bijvoorbeeld de operator ' wrap ' gebruikt `!` (in detail beschreven bij [typen Q# in ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Gelijkheids vergelijking voor `Qubit` waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.
De statussen van de twee qubits worden niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.

Gelijkheids vergelijking voor `Double` waarden kan misleiden door Afrondings effecten.
Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.

Met een wille keurige combi natie van twee numerieke expressies worden de binaire Opera tors `>` ,, `<` `>=` en `<=` kunnen worden gebruikt om een nieuwe booleaanse expressie te maken die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.

Gebruik voor twee Booleaanse expressies de `and` binaire operator om een nieuwe booleaanse expressie te maken die waar is als beide expressies True zijn. Evenzo maakt het gebruik `or` van de operator een expressie die waar is als een van de twee expressies True is.

Aan de hand van een booleaanse expressie `not` kan de unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.

## <a name="string-expressions"></a>Tekenreeksexpressies

Q#Hiermee kunnen teken reeksen worden gebruikt in de `fail` instructie (beschreven in de [controle stroom](xref:microsoft.quantum.guide.controlflow#fail-statement)) en in de [`Message`](xref:microsoft.quantum.intrinsic.message) standaard functie. Het specifieke gedrag van de laatste is afhankelijk van de gebruikte simulator, maar schrijft meestal een bericht naar de host-console wanneer het wordt aangeroepen tijdens een Q# programma.

Teken reeksen in Q# zijn letterlijke waarden of geïnterpoleerde teken reeksen.

Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks van Unicode-tekens tussen dubbele aanhalings symbolen `" "` .
Gebruik in een teken reeks de back slash `\` om een dubbele aanhalings teken () te Escape `\"` of om een nieuwe regel ( `\n` ), een regel terugloop ( `\r` ) of een tab () in te voegen `\t` .
Bijvoorbeeld:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Geïnterpoleerde teken reeksen

De Q# syntaxis voor de teken reeks interpolatie is een subset van de C#-syntaxis. Hieronder vindt u de belangrijkste punten die van toepassing zijn op Q# :

* Als u een letterlijke teken reeks als een geïnterpoleerde teken reeks wilt identificeren, laten voorafgaan door u deze met het `$` symbool. Er mag geen witruimte tussen de `$` en de `"` letterlijke teken reeks worden gestart.

* Hier volgt een voor beeld van een basis voorbeeld waarin de functie wordt gebruikt [`Message`](xref:microsoft.quantum.intrinsic.message) om het resultaat van een meting te schrijven naar de-console, naast andere Q# expressies.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* Een geldige Q# expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.

* Expressies binnen een geïnterpoleerde teken reeks volgen Q# syntaxis, geen C#-syntaxis. Het meest opvallende onderscheid is dat Q# geen ondersteuning biedt voor Verbatim-geïnterpoleerde teken reeksen (multi-line).

Zie [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings)voor meer informatie over de C#-syntaxis.

## <a name="range-expressions"></a>Bereik expressies

`Int` `start` Aan de hand van drie expressies, `step` , en `stop` is de expressie `start .. step .. stop` een bereik expressie waarvan het eerste element, het tweede element, het derde element is `start` , enzovoort `start+step` `start+step+step` , totdat u het wacht `stop` .
Een bereik kan leeg zijn als bijvoorbeeld `step` positief is en `stop < start` .

Het bereik is inclusief aan beide uiteinden. Dat wil zeggen, als het verschil tussen `start` en `stop` een veelvoud van een geheel getal is `step` , dan is het laatste element van het bereik `stop` .

Aan de hand van twee `Int` expressies `start` en `stop` is de expressie `start .. stop` een bereik expressie die gelijk is aan `start .. 1 .. stop` .
Houd er rekening mee dat de geïmpliceerde `step` is + 1, zelfs als `stop` deze kleiner is dan `start` ; in dit geval is het bereik leeg.

Enkele voor beelden van bereiken:

- `1..3`is het bereik van 1, 2, 3.
- `2..2..5`is het bereik van 2, 4.
- `2..2..6`is het bereik 2, 4, 6.
- `6..-2..2`is het bereik van 6, 4, 2.
- `2..1`is een leeg bereik.
- `2..6..7`is het bereik 2.
- `2..2..1`is een leeg bereik.
- `1..-1..2`is een leeg bereik.

## <a name="qubit-expressions"></a>Qubit-expressies

De enige `Qubit` expressies zijn symbolen die zijn gebonden aan `Qubit` waarden of matrix elementen van `Qubit` matrices.
Er zijn geen `Qubit` letterlijke waarden.

## <a name="pauli-expressions"></a>Pauli-expressies

De vier `Pauli` waarden, `PauliI` , `PauliX` , `PauliY` en `PauliZ` zijn allemaal geldige `Pauli` expressies.

Behalve dat zijn de enige `Pauli` expressies symbolen die zijn gebonden aan `Pauli` waarden of matrix elementen van `Pauli` matrices.

## <a name="result-expressions"></a>Resultaat expressies

De twee `Result` waarden `One` en `Zero` zijn geldige `Result` expressies.

Behalve dat zijn de enige `Result` expressies symbolen die zijn gebonden aan `Result` waarden of matrix elementen van `Result` matrices.
Let er met name op dat `One` niet hetzelfde is als het gehele getal `1` en er geen rechtstreekse conversie tussen deze waarden is.
Hetzelfde geldt voor `Zero` en `0` .

## <a name="tuple-expressions"></a>Tuple-expressies

Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen haakjes.
`(1, One)`Is bijvoorbeeld een `(Int, Result)` expressie.

Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.

## <a name="user-defined-type-expressions"></a>Door de gebruiker gedefinieerde type expressies

Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.
Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is op basis van `(Int, Int)` , `IntPair(2, 3)` is dit een geldige letterlijke waarde van dat type.

Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.

## <a name="unwrap-expressions"></a>Onverpakte expressies

In Q# is de operator voor uitpakken een afsluitend uitroep teken `!` .
Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is met het onderliggende type `(Int, Int)` en `s` een variabele met de waarde `IntPair(2, 3)` , dan `s!` is `(2, 3)` .

Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen, kunt u de operator voor uitpakken herhalen. `s!!`Geeft bijvoorbeeld de dubbele waarde onverpakt van aan `s` .
Als is dus `WrappedPair` een door de gebruiker gedefinieerd type met een onderliggend type `IntPair` en `t` een variabele met de waarde `WrappedPair(IntPair(1,2))` , dan `t!!` is `(1,2)` .

De `!` operator heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.
`!`en `[]` positioneel binden; dat wil zeggen, `a[i]![3]` wordt gelezen als `((a[i])!)[3]` : Neem het `i` element van `a` , pak het uit en haal vervolgens het element 3e van de niet-ingepakte waarde op (dit moet een matrix zijn).

De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.
Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.
Bijvoorbeeld:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Matrix expressies

Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen vier Kante haken `[]` .
Alle elementen moeten compatibel zijn met hetzelfde type.

Als er twee matrices van hetzelfde type zijn opgegeven, gebruikt u de binaire `+` operator om een nieuwe matrix te vormen die de samen voeging van de twee matrices vormt.
Bijvoorbeeld `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Matrix maken

Met een type en een `Int` expressie kunt u de `new` operator gebruiken om een nieuwe matrix met de opgegeven grootte toe te wijzen.
`new Int[i + 1]`Wijst bijvoorbeeld een nieuwe `Int` matrix met `i + 1` elementen toe.

Lege letterlijke arrays, zoals `[]` , zijn niet toegestaan.
In plaats daarvan kunt u een matrix met een lengte van nul maken met `new T[0]` , waarbij `T` een tijdelijke aanduiding voor een geschikt type is.

De elementen van een nieuwe matrix worden geïnitialiseerd naar een type-afhankelijke standaard waarde.
In de meeste gevallen is dit een variatie van nul.

Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.
Voor deze typen is de standaard waarde een ongeldige verwijzing die u niet kunt gebruiken zonder dat er een runtime-fout wordt veroorzaakt, vergelijkbaar met een null-verwijzing in talen als C# of Java.
Matrices met qubits of callables moeten worden geïnitialiseerd met niet-standaard waarden voordat u de elementen ervan veilig kunt gebruiken. Zie voor de juiste initialisatie routines <xref:microsoft.quantum.arrays> .

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

Type tuple Initialiseer element-by-element.


### <a name="array-elements"></a>Matrix elementen

Een matrix expressie en een `Int` expressie, vormen een nieuwe expressie met de operator matrix element `[]` .
De nieuwe expressie is van hetzelfde type als het element type van de matrix.
Als bijvoorbeeld `a` is gebonden aan een matrix van het type `Double` , `a[4]` is een `Double` expressie.

Als de matrix expressie geen eenvoudige id is, moet u deze tussen haakjes plaatsen om een element te selecteren.
Als bijvoorbeeld `a` `b` beide matrices van het type zijn `Int` , wordt een element uit de samen voeging als volgt weer gegeven:

```qsharp
(a + b)[13]
```

Alle matrices in Q# zijn gebaseerd op nul.
Dat wil zeggen, het eerste element van een matrix `a` is altijd `a[0]` .


### <a name="array-slices"></a>Matrix segmenten

Een matrix expressie en een `Range` expressie, vormen een nieuwe expressie met de operator matrix segment `[ ]` .
De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die zijn geïndexeerd door de elementen van de `Range` , in de volg orde die is gedefinieerd door de `Range` .
Als bijvoorbeeld `a` is gebonden aan een matrix van het type `Double` , `a[3..-1..0]` is `Double[]` dit een expressie die de eerste vier elementen van `a` , maar in de omgekeerde volg orde bevat zoals ze worden weer gegeven in `a` .

Als het `Range` leeg is, is het resulterende matrix segment geen lengte van nul.

Net als bij het verwijzen naar matrix elementen, moet u de matrix expressie tussen haakjes plaatsen om deze te segmenteren.
Als bijvoorbeeld `a` `b` beide matrices van het type zijn `Int` , wordt een segment uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Uitgestelde begin-en eind waarden

Vanaf onze [0,8-release](xref:microsoft.quantum.relnotes)ondersteunen we context afhankelijke expressies voor bereik segmenting. Met name kunt u de begin-en eind waarden van het bereik weglaten in de context van een expressie voor bereik segmentatie. In dat geval past de compiler de volgende regels toe om de beoogde scheidings tekens voor het bereik af te leiden:

* Als de *begin* waarde van het bereik wordt wegge laten, wordt de uitgestelde begin waarde
  * is nul als er geen stap is opgegeven of de opgegeven stap positief is.  
  * is de lengte van de gesegmenteerde matrix min één als de opgegeven stap negatief is.

* Als de *eind* waarde van het bereik wordt wegge laten, wordt de uitgestelde eind waarde
  * is de lengte van de gesegmenteerde matrix min één als er geen stap is opgegeven of de opgegeven stap positief is.
  * is nul als de opgegeven stap negatief is.

Een aantal voorbeelden:

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

### <a name="copy-and-update-expressions"></a>Expressies kopiëren en bijwerken

Aangezien alle Q# typen waarden zijn (waarbij de qubits een enigszins speciale rol neemt), wordt er formeel een ' Copy ' gemaakt wanneer een waarde aan een symbool is gebonden of wanneer een symbool wordt losgekoppeld. Dat wil zeggen, het gedrag van Q# is hetzelfde als wanneer een kopie is gemaakt met behulp van een toewijzings operator. 

Natuurlijk, in de praktijk, worden alleen de relevante onderdelen opnieuw gemaakt als dat nodig is. Dit is van invloed op hoe u matrices kopieert, omdat het niet mogelijk is om matrix items bij te werken. Voor het wijzigen van een bestaande matrix is een mechanisme voor *kopiëren en bijwerken* vereist.

U kunt een nieuwe matrix maken op basis van een bestaande matrix via de expressies *kopiëren en bijwerken* , die gebruikmaken van de Opera tors `w/` en `<-` .
Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3` , waarbij

* `expression1`moet een type zijn `T[]` voor een bepaald type `T` .
* `expression2`Hiermee wordt gedefinieerd welke indexen in de opgegeven matrix `expression1` worden gewijzigd. `expression2`moet van het type `Int` of van een type zijn `Range` .
* `expression3`is de waarde (n) die wordt gebruikt voor het bijwerken van elementen in `expression1` , op basis van de indices die zijn opgegeven in `expression2` . Als `expression2` is type `Int` , `expression3` moet type zijn `T` . Als `expression2` is type `Range` , `expression3` moet type zijn `T[]` .

De expressie Copy-and-update `arr w/ idx <- value` bouwt bijvoorbeeld een nieuwe matrix met alle elementen die zijn ingesteld op de overeenkomstige elementen in `arr` , met uitzonde ring van het element (en) `idx` dat is opgegeven door, die is ingesteld op de waarde (n) in `value` . 

Opgegeven `arr` bevat de matrix `[0,1,2,3]` en vervolgens 

- `arr w/ 0 <- 10`is de matrix `[10,1,2,3]` .
- `arr w/ 2 <- 10`is de matrix `[0,1,10,3]` .
- `arr w/ 0..2..3 <- [10,12]`is de matrix `[10,1,12,3]` .

#### <a name="copy-and-update-expressions-for-named-items"></a>Expressies kopiëren en bijwerken voor benoemde items

Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen. 

Denk bijvoorbeeld aan het type 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Als `c` de waarde van het type bevat `Complex(1., -1.)` , `c w/ Re <- 0.` is dit een expressie van het type `Complex` waarmee wordt geëvalueerd `Complex(0., -1.)` .

### <a name="jagged-arrays"></a>Gekartelde matrices

Een gekartelde matrix, ook wel een matrix van matrices genoemd, is een matrix waarvan de elementen matrices zijn.
De elementen van een gekartelde matrix kunnen van verschillende grootten zijn.
In het volgende voor beeld ziet u hoe u een gekartelde matrix die een vermenigvuldigings tabel vertegenwoordigt, declareert en initialiseert.

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

### <a name="arrays-of-callables"></a>Matrices van callables 

U kunt ook een matrix van callables maken.

* Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.
* Het element type van de matrix ondersteunt alle [functors](xref:microsoft.quantum.guide.operationsfunctions) die door alle elementen worden ondersteund.
Bijvoorbeeld als `Op1` , `Op2` en `Op3` alle `Qubit[] => Unit` bewerkingen zijn, maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:
  * `[Op1, Op2]`is een matrix met `(Qubit[] => Unit)` bewerkingen.
  * `[Op1, Op3]`is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.
  * `[Op2, Op3]`is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.

Terwijl de bewerkingen `(Qubit[] => Unit is Adj)` en `(Qubit[] => Unit is Ctl)` het gebruikelijke basis type van zijn `(Qubit[] => Unit)` , delen *matrices* van deze bewerkingen echter geen gemeen schappelijk basis type.

Er wordt bijvoorbeeld `[[Op1], [Op2]]` momenteel een fout gegenereerd omdat er wordt geprobeerd een matrix te maken van de twee incompatibele matrix typen `(Qubit[] => Unit is Adj)[]` en `(Qubit[] => Unit is Ctl)[]` .

Zie [aanroep bare expressies](#callable-expressions) op deze pagina of [bewerkingen Q# en functies in ](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie over callables.

## <a name="conditional-expressions"></a>Voorwaardelijke expressies

Er zijn twee expressies van hetzelfde type en een booleaanse expressie die een voorwaardelijke expressie vormen met het vraag teken, `?` en de verticale balk `|` . Gegeven `a==b ? c | d` , is de waarde van de voorwaardelijke expressie `c` als `a==b` waar en `d` als deze False is.

### <a name="conditional-expressions-with-callables"></a>Voorwaardelijke expressies met callables

Voorwaardelijke expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen. In dit geval is het type van de voorwaardelijke expressie een bewerking met invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.
Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[]=>Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:

- `flag ? Op1 | Op2`is een `(Qubit[] => Unit)` bewerking.
- `flag ? Op1 | Op3`is een `(Qubit[] => Unit is Adj)` bewerking.
- `flag ? Op2 | Op3`is een `(Qubit[] => Unit is Ctl)` bewerking.

Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in de waarde van de aanroep. In het geval bijvoorbeeld `a==b ? C(qs) | D(qs)` als `a==b` is waar, wordt de `C` bewerking aangeroepen en als deze ONWAAR is, wordt alleen de `D` bewerking aangeroepen. Deze benadering is vergelijkbaar met *kort circuits* in andere talen.

## <a name="callable-expressions"></a>Aanroep bare expressies

Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik. Een voor beeld `X` is een letterlijke bewerking die verwijst naar de standaard `X` -bibliotheek bewerking en `Message` is een functie-literal die verwijst naar de `Message` functie standaard bibliotheek.

Als een bewerking de `Adjoint` functor ondersteunt, `Adjoint op` is een bewerkings expressie.
Op dezelfde manier geldt dat als de bewerking de `Controlled` functor ondersteunt, `Controlled op` een bewerkings expressie is.
Zie [bewerkings bewerkingen aanroepen](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)voor meer informatie over de typen expressies.

Functors ( `Adjoint` en `Controlled` ) binden meer nauw keuriger dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met `[ ]` .
Daarom zijn de volgende allemaal geldig, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Met type para meter aanroep bare expressies

U kunt een aanroep bare letterlijke waarde gebruiken als een teken reeks, bijvoorbeeld om deze toe te wijzen aan een variabele of door geven aan een andere aanroepable. Als de aanroepable van het [type para meters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)is, moet u in dit geval de para meters opgeven als onderdeel van de aanroep bare waarde.

Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben. Als `Fun` is bijvoorbeeld een functie met de hand tekening `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aanroep bare aanroepende expressies

Gezien een aanroep bare expressie (bewerking of functie) en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kunt u een aanroep *expressie* vormen door de tuple-expressie toe te voegen aan de aanroep bare expressie.
Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.

Als bijvoorbeeld `Op` een bewerking met de hand tekening is `((Int, Qubit) => Double)` , `Op(3, qubit1)` is een expressie van het type `Double` .
Op dezelfde manier `Sin` is als een functie met de hand tekening `(Double -> Double)` `Sin(0.1)` een expressie van het type `Double` .
Ten slotte, als `Builder` een functie met de hand tekening `(Int -> (Int -> Int))` , `Builder(3)` is een functie van `Int` naar `Int` .

Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.
Om het resultaat van aanroepen `Builder` vanuit de vorige alinea te kunnen aanroepen, is de juiste syntaxis:

```qsharp
(Builder(3))(2)
```

Wanneer u een aanroepable van een [type para meter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) aanroept, kunt u de werkelijke type parameters tussen punt haken `< >` na de aanroep bare expressie opgeven.
Deze actie is doorgaans onnodig wanneer de Q# compiler de daad werkelijke typen afleidt.
Het *is* echter wel vereist voor een [gedeeltelijke toepassing](xref:microsoft.quantum.guide.operationsfunctions#partial-application) als een argument van het type para meter left niet is opgegeven.
Het is ook handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.

Als u bijvoorbeeld een `Func` hand tekening `('T1, 'T2, 'T1) -> 'T2` `Op1` hebt en `Op2` hand tekening hebt en hand tekening hebt, `(Qubit[] => Unit is Adj)` moet u als het `Op3` `(Qubit[] => Unit)` `Func` `Op1` eerste argument als `Op2` tweede en `Op3` als derde worden aangeroepen:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

De type specificatie is vereist omdat `Op3` en `Op1` andere typen hebben, waardoor de compiler dit als dubbel zinnig wordt behandeld zonder de specificatie.


## <a name="operator-precedence"></a>Operator prioriteit

* Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^` .

* U kunt `[ ]` voor elke operator een binding maken,, voor het segmenteren en indexeren van matrices.

* De functors `Adjoint` en `Controlled` binding na het indexeren van de matrix, maar vóór alle andere opera tors.

* Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.

Q#Opera tors in volg orde van prioriteit, van hoog naar laag:

Operator | Ariteit | Beschrijving | Typen operand
---------|----------|---------|---------------
 Volg`!` | Unair | Uitpakken | Een door de gebruiker gedefinieerd type
 `-`, `~~~`, `not` | Unair | Numerieke, negatieve, bitsgewijze complement, logische negatie | `Int`, `BigInt` of voor, `Double` of voor `-` `Int` `BigInt` `~~~` , `Bool` voor`not`
 `^` | Binair | Geheel getal energie | `Int`of `BigInt` voor de basis `Int` voor de exponent
 `/`, `*`, `%` | Binair | Deling, vermenigvuldiging, integer modulus | `Int`, `BigInt` of `Double` voor `/` en `*` , `Int` of `BigInt` voor`%`
 `+`, `-` | Binair | Toevoeging of teken reeks-en matrix samenvoeging, aftrekken | `Int`, `BigInt` of `Double` , ook `String` of een matrix type voor`+`
 `<<<`, `>>>` | Binair | Shift-links, Shift-rechts | `Int` of `BigInt`
 `<`, `<=`, `>`, `>=` | Binair | Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen | `Int`, `BigInt` of`Double`
 `==`, `!=` | Binair | gelijk, niet-gelijk-vergelijkingen | een primitief type
 `&&&` | Binair | Bitsgewijze AND | `Int` of `BigInt`
 `^^^` | Binair | Bitsgewijze XOR | `Int` of `BigInt`
 <code>\|\|\|</code> | Binair | Bitsgewijze OR | `Int` of `BigInt`
 `and` | Binair | Logische AND | `Bool`
 `or` | Binair | Logische OR | `Bool`
 `..` | Binair/Ternair | De operator Range | `Int`
 `?` `|` | Ternair | Voorwaardelijk | `Bool`voor de linkerkant
`w/` `<-` | Ternair | Kopiëren en bijwerken | Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)

## <a name="next-steps"></a>Volgende stappen

Nu u kunt werken met expressies in Q# , gaat u naar [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions) voor meer informatie over het definiëren en aanroepen van bewerkingen en functies.
