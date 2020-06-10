---
title: 'Type-expressies in Q #'
description: 'Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: b32644382bb88fb11da00d0d7d78bbd797a0eaaa
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630002"
---
# <a name="type-expressions-in-q"></a>Type-expressies in Q #

## <a name="numeric-expressions"></a>Numerieke expressies

Numerieke expressies zijn expressies van het type `Int` , `BigInt` of `Double` .
Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.

`Int`letterlijke waarden in Q # worden eenvoudigweg geschreven als een reeks cijfers.
Hexadecimale en binaire gehele getallen worden ondersteund met `0x` respectievelijk een en `0b` -voor voegsel.

`BigInt`letterlijke waarden in Q # worden geschreven met een afsluitend `l` of `L` achtervoegsel.
Hexadecimale Big-gehele getallen worden ondersteund met het voor voegsel 0x.
Daarom zijn de volgende geldige toepassingen van `BigInt` letterlijke waarden:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`letterlijke waarden in Q # zijn drijvende-komma getallen die zijn geschreven met decimale cijfers.
Ze kunnen worden geschreven met een decimaal teken, `.` en/of een exponentieel onderdeel dat is aangegeven met e of e (waarna alleen een mogelijk minteken en decimaal tekens geldig zijn).
Hier volgen geldige `Double` letterlijke waarden: `0.0` , `1.2e5` , `1e-5` .

Een expressie met een matrix expressie van elk element type `Int` kan worden gevormd met behulp van de [`Length`](xref:microsoft.quantum.core.length) ingebouwde functie, met de matrix expressie tussen haakjes `(` en `)` .
Als bijvoorbeeld `a` is gebonden aan een matrix, `Length(a)` is dit een expressie met gehele getallen.
Als `b` is een matrix met matrices van gehele getallen, `Int[][]` `Length(b)` is dit het aantal submatrixen in `b` en `Length(b[1])` is het aantal gehele getallen in de tweede submatrix in `b` .

Gegeven twee numerieke expressies van hetzelfde type, de binaire Opera tors `+` , `-` , `*` en `/` kunnen worden gebruikt om een nieuwe numerieke expressie te vormen.
Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.

Als u twee geheeltallige expressies hebt opgegeven, kan de binaire operator `^` (Power) worden gebruikt voor het maken van een nieuwe expressie met gehele getallen.
Dit `^` kan ook worden gebruikt met twee dubbele expressies om een nieuwe dubbele expressie te vormen.
Ten slotte `^` kan worden gebruikt met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant om een nieuwe Big Integer-expressie te vormen.
In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.

Als er twee integere of Big Integer-expressies zijn opgegeven, kan een nieuwe integer of Big Integer-expressie worden gevormd met behulp van de `%` Opera tors (modulus), `&&&` (bitsgewijze en), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR).

Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de rechter kant, de `<<<` (reken kundige Shift-toets links) of de `>>>` Opera tors reken kundig naar rechts kan worden gebruikt om een nieuwe expressie te maken met hetzelfde type als de linker expressie.

De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.
Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.
Als het getal dat moet worden verplaatst een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64` ; dat wil zeggen, een verschuiving van 1 en een verschuiving van 65 hebben hetzelfde effect.

Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.
Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.
Dat wil zeggen dat de ene stap naar links of rechts verschuift precies hetzelfde is als vermenigvuldigen of delen met 2.

Geheel getal delen en integers modulus volgen hetzelfde gedrag voor negatieve getallen als C#.
Dat wil zeggen, heeft `a % b` altijd hetzelfde teken als `a` en is `b * (a / b) + a % b` altijd gelijk aan `a` .
Bijvoorbeeld:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 5 | 2 | -2 | -1
 5 | -2 | 2 | -1

Het delen van een groot geheel getal en modulus werkt op dezelfde manier.

Op basis van een numerieke expressie kan een nieuwe expressie worden gevormd met behulp van de `-` unaire operator.
De nieuwe expressie is van hetzelfde type als de component-expressie.

Een nieuwe expressie van hetzelfde type als een geheel getal of Big Integer-expressie kan worden gevormd met behulp van de `~~~` (bitsgewijze complement) monadische operator.

## <a name="boolean-expressions"></a>Booleaanse expressies

De twee `Bool` letterlijke waarden zijn `true` en `false` .

Op basis van twee expressies van hetzelfde primitieve type `==` kunnen de en `!=` binaire Opera tors worden gebruikt voor het maken van een `Bool` expressie.
De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.

Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken. Als u bijvoorbeeld de operator ' uitpakken ' gebruikt `!` (in detail beschreven bij [typen in Q #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),

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

Met een wille keurige combi natie van twee numerieke expressies worden de binaire Opera tors `>` ,, `<` `>=` en `<=` kunnen worden gebruikt om een nieuwe booleaanse expressie te maken die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.

Aan de hand van twee Booleaanse expressies `and` kunnen de en `or` binaire Opera tors worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als beide (of beide) de twee expressies waar zijn.

Aan de hand van een booleaanse expressie `not` kan de unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.

## <a name="string-expressions"></a>Teken reeks expressies

Q # Hiermee kunnen teken reeksen worden gebruikt in de `fail` instructie (toegelicht bij [controle stroom](xref:microsoft.quantum.guide.controlflow#fail-statement)) en in de [`Message`](xref:microsoft.quantum.intrinsic.message) standaard functie.
Het specifieke gedrag van de laatste is afhankelijk van de gebruikte simulator, maar schrijft meestal een bericht naar de host-console wanneer het wordt aangeroepen tijdens een Q #-programma.

Teken reeksen in Q # zijn letterlijke waarden of geïnterpoleerde teken reeksen.

Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks van Unicode-tekens tussen dubbele citaten, `"` .
In een teken reeks kan de back slash-teken `\` worden gebruikt om een dubbel aanhalings teken te escapen en om een nieuwe regel als een regel `\n` terugloop als en een tab in te voegen als `\r` `\t` .
Bijvoorbeeld:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Geïnterpoleerde teken reeksen

De syntaxis van Q # voor teken reeks-interpolatie is een subset van de C#-syntaxis, maar hier worden de belangrijkste punten voor Q # samenvatten.
De belangrijkste verschillen worden hieronder besproken.

Als u een letterlijke teken reeks als een geïnterpoleerde teken reeks wilt identificeren, laten voorafgaan door u deze met het `$` symbool.
Er mag geen spatie staan tussen de `$` en `"` die een letterlijke teken reeks start.

Hier volgt een voor beeld van een basis voorbeeld waarin de functie wordt gebruikt [`Message`](xref:microsoft.quantum.intrinsic.message) om het resultaat van een meting te schrijven naar de-console, naast andere Q #-expressies.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
Een geldige Q #-expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.

Meer informatie over de C#-syntaxis vindt u in [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).
Het belangrijkste verschil is dat Q # geen Verbatim-geïnterpoleerde teken reeksen ondersteunt.
Expressies binnen een geïnterpoleerde teken reeks volgen Q # syntaxis, geen C#-syntaxis.

## <a name="range-expressions"></a>Bereik expressies

Er zijn drie `Int` expressies `start` , `step` en, `stop` `start .. step .. stop` een bereik expressie waarvan het eerste element, het tweede element, het derde element is `start` `start+step` `start+step+step` , enzovoort, totdat het `stop` wordt door gegeven.
Een bereik kan leeg zijn als bijvoorbeeld `step` positief is en `stop < start` .
Het laatste element van het bereik is `stop` het verschil tussen `start` en `stop` is een integraal veelvoud van `step` ; dat wil zeggen, het bereik is op beide uiteinden.

`Int`Als u twee expressies opgeeft `start` en `stop` , `start .. stop` is dit een bereik expressie die gelijk is aan `start .. 1 .. stop` .
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

Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen `(` en `)` .
Bijvoorbeeld: `(1, One)` is een `(Int, Result)` expressie.

Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.

## <a name="user-defined-type-expressions"></a>Door de gebruiker gedefinieerde type expressies

Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.
Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is op basis van `(Int, Int)` , is `IntPair(2, 3)` dit een geldige letterlijke waarde van dat type.

Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.

## <a name="unwrap-expressions"></a>Onverpakte expressies

In Q # is de operator voor uitpakken een afsluitend uitroep teken `!` .
Zo `IntPair` is bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `(Int, Int)` en was dit `s` een variabele met de waarde `IntPair(2, 3)` `s!` . vervolgens zou het zijn `(2, 3)` .

Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen, kan de operator voor uitpakken worden herhaald. `s!!`Hiermee geeft u bijvoorbeeld de dubbele waarde onverpakt van op `s` .
Als is dus `WrappedPair` een door de gebruiker gedefinieerd type met een onderliggend type `IntPair` en dit `t` is een variabele met de waarde `WrappedPair(IntPair(1,2))` , dan `t!!` zou `(1,2)` .

De `!` operator heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.
`!`en `[]` positioneel binden; dat wil zeggen, `a[i]![3]` moet worden gelezen als `((a[i])!)[3]` : Neem het `i` element van de th, pak het uit `a` en haal vervolgens het derde element van de niet-ingepakte waarde op (dit moet een matrix zijn).

De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.
Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.
Bijvoorbeeld:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Matrix expressies

Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen `[` en `]` .
Alle elementen moeten compatibel zijn met hetzelfde type.

Als er twee matrices van hetzelfde type zijn opgegeven, kan de binaire `+` operator worden gebruikt voor het vormen van een nieuwe matrix die de samen voeging van de twee matrices vormt.
Bijvoorbeeld: `[1,2,3] + [4,5,6]` `[1,2,3,4,5,6]` .

### <a name="array-creation"></a>Matrix maken

Op basis van een type en een `Int` expressie `new` kan de operator worden gebruikt voor het toewijzen van een nieuwe matrix met de opgegeven grootte.
Bijvoorbeeld, `new Int[i + 1]` zou een nieuwe `Int` matrix met elementen kunnen toewijzen `i + 1` .

Lege letterlijke arrays, `[]` , zijn niet toegestaan.
In plaats daarvan `new ★[0]` kunt u, waar `★` als tijdelijke aanduiding voor een geschikt type, de gewenste matrix met een lengte van nul maken.

De elementen van een nieuwe matrix worden geïnitialiseerd op een type-afhankelijke standaard waarde.
In de meeste gevallen is dit een bepaalde variatie van nul.

Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.
Daarom is de standaard waarde voor deze typen een ongeldige verwijzing die niet kan worden gebruikt zonder dat er een runtime-fout wordt veroorzaakt.
Dit is vergelijkbaar met een null-verwijzing in talen als C# of Java.
Matrices met qubits of callables moeten correct worden geïnitialiseerd met niet-standaard waarden voordat de elementen veilig kunnen worden gebruikt. Geschikte initialisatie routines kunt u vinden in <xref:microsoft.quantum.arrays> .

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


### <a name="array-elements"></a>Matrix elementen

Met een matrix expressie en een `Int` expressie kan een nieuwe expressie worden gevormd met de `[` operator and van het `]` matrix element.
De nieuwe expressie is van hetzelfde type als het element type van de matrix.
Als bijvoorbeeld `a` is gebonden aan een matrix van `Double` s, dan `a[4]` is een `Double` expressie.

Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om een element te selecteren.
Als bijvoorbeeld `a` `b` beide matrices van `Int` s zijn, wordt een element uit de samen voeging als volgt weer gegeven:

```qsharp
(a + b)[13]
```

Alle matrices in Q # zijn gebaseerd op nul.
Dat wil zeggen, het eerste element van een matrix `a` is altijd `a[0]` .


### <a name="array-slices"></a>Matrix segmenten

Met een matrix expressie en een `Range` expressie kan een nieuwe expressie worden gevormd met behulp van de `[` operator en de `]` matrix segment.
De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die worden geïndexeerd door de elementen van de `Range` , in de volg orde die is gedefinieerd door de `Range` .
Als bijvoorbeeld `a` is gebonden aan een matrix van `Double` s, `a[3..-1..0]` is `Double[]` dit een expressie die de eerste vier elementen van `a` , maar in de omgekeerde volg orde bevat zoals ze worden weer gegeven in `a` .

Als het `Range` leeg is, is het resulterende matrix segment nul lengte.

Net als bij het verwijzen naar matrix elementen als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om te kunnen worden gesegmenteerd.
Als `a` en `b` beide matrices van `Int` s, wordt een segment uit de samen voeging als volgt weer gegeven:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Uitgestelde begin-en eind waarden

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

### <a name="copy-and-update-expressions"></a>Expressies kopiëren en bijwerken

Omdat alle typen Q # waardetypen zijn, waarbij de qubits een enigszins speciale rol neemt, wordt formeel een ' Copy ' gemaakt wanneer een waarde is gebonden aan een symbool of wanneer een symbool wordt losgekoppeld. Dat wil zeggen dat het gedrag van Q # hetzelfde is als wanneer er een kopie is gemaakt voor de toewijzing.
Natuurlijk worden alleen de relevante onderdelen, indien nodig, feitelijk opnieuw gemaakt. 

Dit bevat met name ook matrices.
Met name het is niet mogelijk om matrix items bij te werken. Voor het wijzigen van een bestaande matrix is een mechanisme voor *kopiëren en bijwerken* vereist.

Nieuwe matrices kunnen worden gemaakt op basis van bestaande met behulp van *Copy-en-update-* expressies.
Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3` , waarbij `expression1` type `T[]` voor een type is `T` .
De tweede `expression2` definieert de indices van de element (en) die moeten worden gewijzigd vergeleken met de matrix in en moet van het type `expression1` `Int` of van het type zijn `Range` .
Als `expression2` is van `Int` het type, moet `expression3` van het type zijn `T` . Als `expression2` is van `Range` het type, moet `expression3` van het type zijn `T[]` .

Met een copy-and-update-expressie wordt `arr w/ idx <- value` een nieuwe matrix gemaakt met alle elementen die zijn ingesteld op het overeenkomstige element in `arr` , met uitzonde ring van het element (en) op `idx` , die zijn ingesteld op een of meer in `value` . Als bijvoorbeeld `arr` een matrix bevat `[0,1,2,3]` , 
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

Meer informatie over oproep bare typen vindt u hieronder en op de volgende pagina, [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions).

Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.
Het element type van de matrix ondersteunt alle functors die door alle elementen worden ondersteund.
Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[] => Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:

- `[Op1, Op2]`is een matrix met `(Qubit[] => Unit)` bewerkingen.
- `[Op1, Op3]`is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.
- `[Op2, Op3]`is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.

Hoewel `(Qubit[] => Unit is Adj)` en bewerkingen echter `(Qubit[] => Unit is Ctl)` het gemeen schappelijke basis type hebben `(Qubit[] => Unit)` , is het niet mogelijk dat matrices *van* deze opera tors een gemeen schappelijk basis type hebben. Er wordt bijvoorbeeld `[[Op1], [Op2]]` momenteel een fout gegenereerd omdat er wordt geprobeerd een matrix te maken van de incompatibele matrix typen `(Qubit[] => Unit is Adj)[]` en `(Qubit[] => Unit is Ctl)[]` .


## <a name="conditional-expressions"></a>Voorwaardelijke expressies

Als er twee andere expressies van hetzelfde type en een booleaanse expressie zijn opgegeven, kan de voorwaardelijke expressie worden gevormd met behulp van het vraag teken `?` en de verticale balk `|` .
Bijvoorbeeld `a==b ? c | d`.
In dit voor beeld is de waarde van de voorwaardelijke expressie `c` als `a==b` True en `d` als deze False is.

### <a name="conditional-expressions-with-callables"></a>Voorwaardelijke expressies met callables

De twee expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.
In dit geval is het type van de voorwaardelijke expressie een bewerking met de invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.
Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[]=>Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:

- `flag ? Op1 | Op2`is een `(Qubit[] => Unit)` bewerking.
- `flag ? Op1 | Op3`is een `(Qubit[] => Unit is Adj)` bewerking.
- `flag ? Op2 | Op3`is een `(Qubit[] => Unit is Ctl)` bewerking.

Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in het resultaat dat de waarde van de aanroep zal zijn.
Als bijvoorbeeld is ingesteld op `a==b ? C(qs) | D(qs)` True, wordt `a==b` de `C` bewerking opgeroepen en als deze ONWAAR is, `D` wordt alleen aangeroepen.
Dit is vergelijkbaar met kort circuits in andere talen.

## <a name="callable-expressions"></a>Aanroep bare expressies

Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.
Bijvoorbeeld: `X` is een letterlijke bewerkings bewerking die verwijst naar de standaard `X` -bibliotheek bewerking en `Message` is een functie-literal die verwijst naar de functie standaard bibliotheek `Message` .

Als een bewerking de `Adjoint` functor ondersteunt, `Adjoint op` is een bewerkings expressie.
Op dezelfde manier geldt dat als de bewerking de `Controlled` functor ondersteunt, `Controlled op` een bewerkings expressie is.
De typen van deze expressies worden opgegeven bij het [aanroepen van bewerkings-specials](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).

Functors ( `Adjoint` en `Controlled` ) binden meer nauw keuriger dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met [].
Daarom is het volgende juridisch, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Met type para meter aanroep bare expressies

Een aanroep bare letterlijke tekenloze kan worden gebruikt als een waarde, moet worden toegewezen aan een variabele of door gegeven aan een andere aanroepable.
Als de aanroepable van het [type para meters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)is, moeten deze als onderdeel van de aanroep bare waarde worden opgegeven.
Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben.

Als bijvoorbeeld `Fun` een functie met hand tekening is `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aanroep bare aanroepende expressies

Gezien een aanroep bare (Operation-of Function-) expressie en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kan een aanroep expressie worden gevormd door de tuple-expressie toe te voegen aan de aanroep bare expressie.
Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.

Als bijvoorbeeld `Op` een bewerking met hand tekening is `((Int, Qubit) => Double)` , `Op(3, qubit1)` is een expressie van het type `Double` .
Op dezelfde manier `Sin` is, als een functie met hand tekening `(Double -> Double)` , `Sin(0.1)` een expressie van het type `Double` .
Ten slotte, als `Builder` een functie met hand tekening `(Int -> (Int -> Int))` , `Builder(3)` is een functie van naar int.

Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.
Om het resultaat van aanroepen `Builder` vanuit de vorige alinea te kunnen aanroepen, is de juiste syntaxis:

```qsharp
(Builder(3))(2)
```

Bij het aanroepen van een aanroep [bare type para meter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) kunnen de werkelijke type parameters worden opgegeven tussen punt haken `<` en `>` na de aanroep bare expressie.
Dit is doorgaans onnodig omdat de compiler Q # de daad werkelijke typen afleidt.
Het *is* echter wel vereist voor een [gedeeltelijke toepassing](xref:microsoft.quantum.guide.operationsfunctions#partial-application) als een argument van het type para meter left niet is opgegeven.
Het is ook soms handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.

Bijvoorbeeld als `Func` hand tekening is ondertekend `('T1, 'T2, 'T1) -> 'T2` , `Op1` hand tekening heeft `Op2` `(Qubit[] => Unit is Adj)` en `Op3` hand tekening heeft, om als het `(Qubit[] => Unit)` `Func` `Op1` eerste argument `Op2` als tweede en `Op3` als derde te worden aangeroepen:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

De type specificatie is vereist omdat `Op3` en `Op1` andere typen hebben, waardoor de compiler dit als dubbel zinnig wordt behandeld zonder de specificatie.


## <a name="operator-precedence"></a>Operator prioriteit

Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^` .

U kunt `[` `]` voor elke operator een binding maken, en voor het segmenteren en indexeren van matrices.

De functors `Adjoint` en `Controlled` binding na het indexeren van de matrix, maar vóór alle andere opera tors.

Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.

Opera tors in volg orde van prioriteit, van hoog naar laag:

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

Nu u met de expressies in Q # kunt werken, kunt u de [bewerkingen en functies in q #](xref:microsoft.quantum.guide.operationsfunctions) gebruiken om te leren hoe u bewerkingen en functies definieert en aanroept.
