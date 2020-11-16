---
title: 'Expressies in Q#'
description: 'Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q# .'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e95a7cb9b74136ef9a6f51b4bbc32d1d93c43a0d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691594"
---
# <a name="expressions-in-no-locq"></a><span data-ttu-id="484a9-103">Expressies in Q#</span><span class="sxs-lookup"><span data-stu-id="484a9-103">Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="484a9-104">Numerieke expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-104">Numeric Expressions</span></span>

<span data-ttu-id="484a9-105">Numerieke expressies zijn expressies van het type `Int` , `BigInt` of `Double` .</span><span class="sxs-lookup"><span data-stu-id="484a9-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="484a9-106">Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="484a9-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="484a9-107">`Int` letterlijke waarden in Q# worden geschreven als een reeks cijfers.</span><span class="sxs-lookup"><span data-stu-id="484a9-107">`Int` literals in Q# are written as a sequence of digits.</span></span>
<span data-ttu-id="484a9-108">Hexadecimale en binaire gehele getallen worden ondersteund en worden met `0x` respectievelijk een en `0b` -voor voegsel geschreven.</span><span class="sxs-lookup"><span data-stu-id="484a9-108">Hexadecimal and binary integers are supported and written with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="484a9-109">`BigInt` letterlijke waarden in Q# hebben een navolgende `l` of `L` achtervoegsel.</span><span class="sxs-lookup"><span data-stu-id="484a9-109">`BigInt` literals in Q# have a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="484a9-110">Hexadecimale Big gehele getallen worden ondersteund en geschreven met het voor voegsel ' 0x '.</span><span class="sxs-lookup"><span data-stu-id="484a9-110">Hexadecimal big integers are supported and written with a "0x" prefix.</span></span>
<span data-ttu-id="484a9-111">Daarom zijn de volgende geldige toepassingen van `BigInt` letterlijke waarden:</span><span class="sxs-lookup"><span data-stu-id="484a9-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="484a9-112">`Double` letterlijke waarden in Q# zijn drijvende-komma getallen die zijn geschreven met decimale cijfers.</span><span class="sxs-lookup"><span data-stu-id="484a9-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="484a9-113">Ze kunnen worden geschreven met of zonder een decimaal teken, `.` of een exponentieel onderdeel dat is aangegeven met e of e (waarna alleen een mogelijk minteken en decimaal tekens geldig zijn).</span><span class="sxs-lookup"><span data-stu-id="484a9-113">They can be written with or without a decimal point, `.`, or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="484a9-114">Hier volgen geldige `Double` letterlijke waarden: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="484a9-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="484a9-115">Op basis van een matrix expressie van elk element type kunt u een `Int` expressie maken met behulp van de [`Length`](xref:Microsoft.Quantum.Core.Length) ingebouwde functie, waarbij de matrix expressie tussen haakjes staat.</span><span class="sxs-lookup"><span data-stu-id="484a9-115">Given an array expression of any element type, you can form an `Int` expression using the [`Length`](xref:Microsoft.Quantum.Core.Length) built-in function, with the array expression enclosed in parentheses.</span></span>
<span data-ttu-id="484a9-116">Als bijvoorbeeld `a` is gebonden aan een matrix, `Length(a)` is dit een expressie met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="484a9-116">For example, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="484a9-117">Als `b` is een matrix met matrices van gehele getallen, `Int[][]` `Length(b)` is dit het aantal submatrixen in `b` en `Length(b[1])` is het aantal gehele getallen in de tweede submatrix in `b` .</span><span class="sxs-lookup"><span data-stu-id="484a9-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="484a9-118">Gegeven twee numerieke expressies van hetzelfde type, de binaire Opera tors `+` , `-` , `*` en `/` kunnen worden gebruikt om een nieuwe numerieke expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="484a9-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="484a9-119">Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.</span><span class="sxs-lookup"><span data-stu-id="484a9-119">The type of the new expression is the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="484a9-120">Als u twee geheeltallige expressies hebt opgegeven, gebruikt u de binaire operator `^` (Power) om een nieuwe expressie met gehele getallen te vormen.</span><span class="sxs-lookup"><span data-stu-id="484a9-120">Given two integer expressions, use the binary operator `^` (power) to form a new integer expression.</span></span>
<span data-ttu-id="484a9-121">U kunt ook `^` met twee dubbele expressies gebruiken om een nieuwe dubbele expressie te maken.</span><span class="sxs-lookup"><span data-stu-id="484a9-121">Similarly, you can also use `^` with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="484a9-122">Ten slotte kunt u `^` met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant gebruiken om een nieuwe Big Integer-expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="484a9-122">Finally, you can use `^` with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="484a9-123">In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="484a9-123">In this case, the second parameter must fit into 32 bits; if not, it raises a runtime error.</span></span>

<span data-ttu-id="484a9-124">Als er twee integere of Big Integer-expressies zijn, moet u een nieuwe geheel getal of Big Integer-expressie vormen met behulp van de `%` Opera tors (modulus), `&&&` (bitsgewijze en), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR).</span><span class="sxs-lookup"><span data-stu-id="484a9-124">Given two integer or big integer expressions, form a new integer or big integer expression using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="484a9-125">Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de rechter kant, gebruik de `<<<` (reken kundige verschuiving links) of `>>>` (reken kundige Shift-rechts) om een nieuwe expressie te maken met hetzelfde type als de linker expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-125">Given either an integer or big integer expression on the left, and an integer expression on the right, use the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="484a9-126">De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="484a9-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="484a9-127">Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="484a9-127">The shift amount for either shift operation must also fit into 32 bits; if not, it raises a runtime error.</span></span>
<span data-ttu-id="484a9-128">Als het getal verschuiven een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64` ; dat wil zeggen, een verschuiving van 1 en een verschuiving van 65 hebben hetzelfde effect.</span><span class="sxs-lookup"><span data-stu-id="484a9-128">If the number shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="484a9-129">Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.</span><span class="sxs-lookup"><span data-stu-id="484a9-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="484a9-130">Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.</span><span class="sxs-lookup"><span data-stu-id="484a9-130">Shifting a negative value either left or right results in a negative number.</span></span>
<span data-ttu-id="484a9-131">Dat wil zeggen dat de ene stap naar links of rechts verschuift, hetzelfde is als vermenigvuldigen of delen met 2.</span><span class="sxs-lookup"><span data-stu-id="484a9-131">That is, shifting one step to the left or right is the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="484a9-132">Geheel getal delen en integers modulus volgen hetzelfde gedrag voor negatieve getallen als C#.</span><span class="sxs-lookup"><span data-stu-id="484a9-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span> <span data-ttu-id="484a9-133">Dat wil zeggen, `a % b` heeft altijd hetzelfde teken als `a` en is `b * (a / b) + a % b` altijd gelijk aan `a` .</span><span class="sxs-lookup"><span data-stu-id="484a9-133">That is, `a % b` always has the same sign as `a`, and `b * (a / b) + a % b` always equals `a`.</span></span> <span data-ttu-id="484a9-134">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="484a9-134">For example:</span></span>

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| <span data-ttu-id="484a9-135">5</span><span class="sxs-lookup"><span data-stu-id="484a9-135">5</span></span> | <span data-ttu-id="484a9-136">2</span><span class="sxs-lookup"><span data-stu-id="484a9-136">2</span></span> | <span data-ttu-id="484a9-137">2</span><span class="sxs-lookup"><span data-stu-id="484a9-137">2</span></span> | <span data-ttu-id="484a9-138">1</span><span class="sxs-lookup"><span data-stu-id="484a9-138">1</span></span> |
| <span data-ttu-id="484a9-139">5</span><span class="sxs-lookup"><span data-stu-id="484a9-139">5</span></span> | <span data-ttu-id="484a9-140">-2</span><span class="sxs-lookup"><span data-stu-id="484a9-140">-2</span></span> | <span data-ttu-id="484a9-141">-2</span><span class="sxs-lookup"><span data-stu-id="484a9-141">-2</span></span> | <span data-ttu-id="484a9-142">1</span><span class="sxs-lookup"><span data-stu-id="484a9-142">1</span></span> |
| <span data-ttu-id="484a9-143">5</span><span class="sxs-lookup"><span data-stu-id="484a9-143">-5</span></span> | <span data-ttu-id="484a9-144">2</span><span class="sxs-lookup"><span data-stu-id="484a9-144">2</span></span> | <span data-ttu-id="484a9-145">-2</span><span class="sxs-lookup"><span data-stu-id="484a9-145">-2</span></span> | <span data-ttu-id="484a9-146">-1</span><span class="sxs-lookup"><span data-stu-id="484a9-146">-1</span></span> |
| <span data-ttu-id="484a9-147">5</span><span class="sxs-lookup"><span data-stu-id="484a9-147">-5</span></span> | <span data-ttu-id="484a9-148">-2</span><span class="sxs-lookup"><span data-stu-id="484a9-148">-2</span></span> | <span data-ttu-id="484a9-149">2</span><span class="sxs-lookup"><span data-stu-id="484a9-149">2</span></span> | <span data-ttu-id="484a9-150">-1</span><span class="sxs-lookup"><span data-stu-id="484a9-150">-1</span></span> |

<span data-ttu-id="484a9-151">Groot geheel getal delen en modulus bewerkingen werken op dezelfde manier.</span><span class="sxs-lookup"><span data-stu-id="484a9-151">Big integer division and modulus operations work the same way.</span></span>

<span data-ttu-id="484a9-152">Met een wille keurige numerieke expressie kunt u een nieuwe expressie maken met behulp van de `-` unaire operator.</span><span class="sxs-lookup"><span data-stu-id="484a9-152">Given any numeric expression, you can form a new expression using the `-` unary operator.</span></span>
<span data-ttu-id="484a9-153">De nieuwe expressie is van hetzelfde type als de onderdeel expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-153">The new expression is the same type as the constituent expression.</span></span>

<span data-ttu-id="484a9-154">Als een geheel getal of een Big Integer-expressie, kunt u een nieuwe expressie van hetzelfde type vormen met behulp van de `~~~` (bitsgewijze complement) monadische operator.</span><span class="sxs-lookup"><span data-stu-id="484a9-154">Given any integer or big integer expression, you can form a new expression of the same type using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="484a9-155">Booleaanse expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-155">Boolean Expressions</span></span>

<span data-ttu-id="484a9-156">De twee `Bool` letterlijke waarden zijn `true` en `false` .</span><span class="sxs-lookup"><span data-stu-id="484a9-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="484a9-157">Op basis van twee expressies van hetzelfde primitieve type `==` kunnen de en `!=` binaire Opera tors worden gebruikt voor het maken van een `Bool` expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="484a9-158">De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.</span><span class="sxs-lookup"><span data-stu-id="484a9-158">The expression is true if the two expressions are equal and false if not.</span></span>

<span data-ttu-id="484a9-159">Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="484a9-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="484a9-160">Als u bijvoorbeeld de operator ' wrap ' gebruikt `!` (in detail beschreven bij [typen Q# in ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span><span class="sxs-lookup"><span data-stu-id="484a9-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="484a9-161">Gelijkheids vergelijking voor `Qubit` waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.</span><span class="sxs-lookup"><span data-stu-id="484a9-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="484a9-162">De statussen van de twee qubits worden niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.</span><span class="sxs-lookup"><span data-stu-id="484a9-162">The states of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="484a9-163">Gelijkheids vergelijking voor `Double` waarden kan misleiden door Afrondings effecten.</span><span class="sxs-lookup"><span data-stu-id="484a9-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="484a9-164">Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="484a9-164">For example, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="484a9-165">Met een wille keurige combi natie van twee numerieke expressies worden de binaire Opera tors `>` ,, `<` `>=` en `<=` kunnen worden gebruikt om een nieuwe booleaanse expressie te maken die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="484a9-166">Gebruik voor twee Booleaanse expressies de `and` binaire operator om een nieuwe booleaanse expressie te maken die waar is als beide expressies True zijn.</span><span class="sxs-lookup"><span data-stu-id="484a9-166">Given any two Boolean expressions, use the `and` binary operator to construct a new Boolean expression that is true if both of the two expressions are true.</span></span> <span data-ttu-id="484a9-167">Evenzo maakt het gebruik `or` van de operator een expressie die waar is als een van de twee expressies True is.</span><span class="sxs-lookup"><span data-stu-id="484a9-167">Likewise, using the `or` operator creates an expression that is true if either of the two expressions is true.</span></span>

<span data-ttu-id="484a9-168">Aan de hand van een booleaanse expressie `not` kan de unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.</span><span class="sxs-lookup"><span data-stu-id="484a9-168">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="484a9-169">Tekenreeksexpressies</span><span class="sxs-lookup"><span data-stu-id="484a9-169">String expressions</span></span>

<span data-ttu-id="484a9-170">Q# Hiermee kunnen teken reeksen worden gebruikt in de `fail` instructie (beschreven in de [controle stroom](xref:microsoft.quantum.guide.controlflow#fail-statement)) en in de [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) standaard functie.</span><span class="sxs-lookup"><span data-stu-id="484a9-170">Q# allows strings to be used in the `fail` statement (explained in [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) standard function.</span></span> <span data-ttu-id="484a9-171">Het specifieke gedrag van de laatste is afhankelijk van de gebruikte simulator, maar schrijft meestal een bericht naar de host-console wanneer het wordt aangeroepen tijdens een Q# programma.</span><span class="sxs-lookup"><span data-stu-id="484a9-171">The specific behavior of the latter depends on the simulator used but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="484a9-172">Teken reeksen in Q# zijn letterlijke waarden of geïnterpoleerde teken reeksen.</span><span class="sxs-lookup"><span data-stu-id="484a9-172">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="484a9-173">Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks van Unicode-tekens tussen dubbele aanhalings symbolen `" "` .</span><span class="sxs-lookup"><span data-stu-id="484a9-173">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double-quotes `" "`.</span></span>
<span data-ttu-id="484a9-174">Gebruik in een teken reeks de back slash `\` om een dubbele aanhalings teken () te Escape `\"` of om een nieuwe regel ( `\n` ), een regel terugloop ( `\r` ) of een tab () in te voegen `\t` .</span><span class="sxs-lookup"><span data-stu-id="484a9-174">Inside of a string, use the backslash character `\` to escape a double-quote character (`\"`), or to insert a new-line ( `\n` ), a carriage return (`\r`), or a tab (`\t`).</span></span>
<span data-ttu-id="484a9-175">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="484a9-175">For example:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="484a9-176">Geïnterpoleerde teken reeksen</span><span class="sxs-lookup"><span data-stu-id="484a9-176">Interpolated strings</span></span>

<span data-ttu-id="484a9-177">De Q# syntaxis voor de teken reeks interpolatie is een subset van de C#-syntaxis.</span><span class="sxs-lookup"><span data-stu-id="484a9-177">The Q# syntax for string interpolations is a subset of the C# syntax.</span></span> <span data-ttu-id="484a9-178">Hieronder vindt u de belangrijkste punten die van toepassing zijn op Q# :</span><span class="sxs-lookup"><span data-stu-id="484a9-178">Following are the key points as they pertain to Q#:</span></span>

* <span data-ttu-id="484a9-179">Als u een letterlijke teken reeks als een geïnterpoleerde teken reeks wilt identificeren, laten voorafgaan door u deze met het `$` symbool.</span><span class="sxs-lookup"><span data-stu-id="484a9-179">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span> <span data-ttu-id="484a9-180">Er mag geen witruimte tussen de `$` en de `"` letterlijke teken reeks worden gestart.</span><span class="sxs-lookup"><span data-stu-id="484a9-180">There can be no white space between the `$` and the `"` that starts a string literal.</span></span>

* <span data-ttu-id="484a9-181">Hier volgt een voor beeld van een basis voorbeeld waarin de functie wordt gebruikt [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) om het resultaat van een meting te schrijven naar de-console, naast andere Q# expressies.</span><span class="sxs-lookup"><span data-stu-id="484a9-181">The following is a basic example using the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* <span data-ttu-id="484a9-182">Een geldige Q# expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.</span><span class="sxs-lookup"><span data-stu-id="484a9-182">Any valid Q# expression may appear in an interpolated string.</span></span>

* <span data-ttu-id="484a9-183">Expressies binnen een geïnterpoleerde teken reeks volgen Q# syntaxis, geen C#-syntaxis.</span><span class="sxs-lookup"><span data-stu-id="484a9-183">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span> <span data-ttu-id="484a9-184">Het meest opvallende onderscheid is dat Q# geen ondersteuning biedt voor Verbatim-geïnterpoleerde teken reeksen (multi-line).</span><span class="sxs-lookup"><span data-stu-id="484a9-184">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>

<span data-ttu-id="484a9-185">Zie [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings)voor meer informatie over de C#-syntaxis.</span><span class="sxs-lookup"><span data-stu-id="484a9-185">For more details about the C# syntax, see [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>

## <a name="range-expressions"></a><span data-ttu-id="484a9-186">Bereik expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-186">Range Expressions</span></span>

<span data-ttu-id="484a9-187">`Int` `start` Aan de hand van drie expressies, `step` , en `stop` is de expressie `start .. step .. stop` een bereik expressie waarvan het eerste element, het tweede element, het derde element is `start` , enzovoort `start+step` `start+step+step` , totdat u het wacht `stop` .</span><span class="sxs-lookup"><span data-stu-id="484a9-187">Given any three `Int` expressions `start`, `step`, and `stop`, the expression `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, and so on, until you pass `stop`.</span></span>
<span data-ttu-id="484a9-188">Een bereik kan leeg zijn als bijvoorbeeld `step` positief is en `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="484a9-188">A range may be empty if, for example, `step` is positive and `stop < start`.</span></span>

<span data-ttu-id="484a9-189">Het bereik is inclusief aan beide uiteinden.</span><span class="sxs-lookup"><span data-stu-id="484a9-189">The range is inclusive at both ends.</span></span> <span data-ttu-id="484a9-190">Dat wil zeggen, als het verschil tussen `start` en `stop` een veelvoud van een geheel getal is `step` , dan is het laatste element van het bereik `stop` .</span><span class="sxs-lookup"><span data-stu-id="484a9-190">That is, if the difference between `start` and `stop` is an integer multiple of `step`, the last element of the range will be `stop`.</span></span>

<span data-ttu-id="484a9-191">Aan de hand van twee `Int` expressies `start` en `stop` is de expressie `start .. stop` een bereik expressie die gelijk is aan `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="484a9-191">Given any two `Int` expressions `start` and `stop`, the expression `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="484a9-192">Houd er rekening mee dat de geïmpliceerde `step` is + 1, zelfs als `stop` deze kleiner is dan `start` ; in dit geval is het bereik leeg.</span><span class="sxs-lookup"><span data-stu-id="484a9-192">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="484a9-193">Enkele voor beelden van bereiken:</span><span class="sxs-lookup"><span data-stu-id="484a9-193">Some example ranges are:</span></span>

- <span data-ttu-id="484a9-194">`1..3` is het bereik van 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="484a9-194">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="484a9-195">`2..2..5` is het bereik van 2, 4.</span><span class="sxs-lookup"><span data-stu-id="484a9-195">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="484a9-196">`2..2..6` is het bereik 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="484a9-196">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="484a9-197">`6..-2..2` is het bereik van 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="484a9-197">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="484a9-198">`2..1` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="484a9-198">`2..1` is the empty range.</span></span>
- <span data-ttu-id="484a9-199">`2..6..7` is het bereik 2.</span><span class="sxs-lookup"><span data-stu-id="484a9-199">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="484a9-200">`2..2..1` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="484a9-200">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="484a9-201">`1..-1..2` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="484a9-201">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="484a9-202">Qubit-expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-202">Qubit Expressions</span></span>

<span data-ttu-id="484a9-203">De enige `Qubit` expressies zijn symbolen die zijn gebonden aan `Qubit` waarden of matrix elementen van `Qubit` matrices.</span><span class="sxs-lookup"><span data-stu-id="484a9-203">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="484a9-204">Er zijn geen `Qubit` letterlijke waarden.</span><span class="sxs-lookup"><span data-stu-id="484a9-204">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="484a9-205">Pauli-expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-205">Pauli Expressions</span></span>

<span data-ttu-id="484a9-206">De vier `Pauli` waarden, `PauliI` , `PauliX` , `PauliY` en `PauliZ` zijn allemaal geldige `Pauli` expressies.</span><span class="sxs-lookup"><span data-stu-id="484a9-206">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="484a9-207">Behalve dat zijn de enige `Pauli` expressies symbolen die zijn gebonden aan `Pauli` waarden of matrix elementen van `Pauli` matrices.</span><span class="sxs-lookup"><span data-stu-id="484a9-207">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="484a9-208">Resultaat expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-208">Result Expressions</span></span>

<span data-ttu-id="484a9-209">De twee `Result` waarden `One` en `Zero` zijn geldige `Result` expressies.</span><span class="sxs-lookup"><span data-stu-id="484a9-209">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="484a9-210">Behalve dat zijn de enige `Result` expressies symbolen die zijn gebonden aan `Result` waarden of matrix elementen van `Result` matrices.</span><span class="sxs-lookup"><span data-stu-id="484a9-210">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="484a9-211">Let er met name op dat `One` niet hetzelfde is als het gehele getal `1` en er geen rechtstreekse conversie tussen deze waarden is.</span><span class="sxs-lookup"><span data-stu-id="484a9-211">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="484a9-212">Hetzelfde geldt voor `Zero` en `0` .</span><span class="sxs-lookup"><span data-stu-id="484a9-212">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="484a9-213">Tuple-expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-213">Tuple Expressions</span></span>

<span data-ttu-id="484a9-214">Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen haakjes.</span><span class="sxs-lookup"><span data-stu-id="484a9-214">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in parentheses.</span></span>
<span data-ttu-id="484a9-215">`(1, One)`Is bijvoorbeeld een `(Int, Result)` expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-215">For example, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="484a9-216">Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.</span><span class="sxs-lookup"><span data-stu-id="484a9-216">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="484a9-217">Type expressies van User-Defined</span><span class="sxs-lookup"><span data-stu-id="484a9-217">User-Defined Type Expressions</span></span>

<span data-ttu-id="484a9-218">Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.</span><span class="sxs-lookup"><span data-stu-id="484a9-218">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="484a9-219">Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is op basis van `(Int, Int)` , `IntPair(2, 3)` is dit een geldige letterlijke waarde van dat type.</span><span class="sxs-lookup"><span data-stu-id="484a9-219">For example, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` is a valid literal of that type.</span></span>

<span data-ttu-id="484a9-220">Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.</span><span class="sxs-lookup"><span data-stu-id="484a9-220">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="484a9-221">Onverpakte expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-221">Unwrap Expressions</span></span>

<span data-ttu-id="484a9-222">In Q# is de operator voor uitpakken een afsluitend uitroep teken `!` .</span><span class="sxs-lookup"><span data-stu-id="484a9-222">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="484a9-223">Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is met het onderliggende type `(Int, Int)` en `s` een variabele met de waarde `IntPair(2, 3)` , dan `s!` is `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="484a9-223">For example, if `IntPair` is a user-defined type with the underlying type `(Int, Int)` and `s` is a variable with value `IntPair(2, 3)`, then `s!` is `(2, 3)`.</span></span>

<span data-ttu-id="484a9-224">Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen, kunt u de operator voor uitpakken herhalen.</span><span class="sxs-lookup"><span data-stu-id="484a9-224">For user-defined types defined in terms of other user-defined types, you can repeat the unwrap operator.</span></span> <span data-ttu-id="484a9-225">`s!!`Geeft bijvoorbeeld de dubbele waarde onverpakt van aan `s` .</span><span class="sxs-lookup"><span data-stu-id="484a9-225">For example, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="484a9-226">Als is dus `WrappedPair` een door de gebruiker gedefinieerd type met een onderliggend type `IntPair` en `t` een variabele met de waarde `WrappedPair(IntPair(1,2))` , dan `t!!` is `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="484a9-226">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` is `(1,2)`.</span></span>

<span data-ttu-id="484a9-227">De `!` operator heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.</span><span class="sxs-lookup"><span data-stu-id="484a9-227">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="484a9-228">`!` en `[]` positioneel binden; dat wil zeggen, `a[i]![3]` wordt gelezen als `((a[i])!)[3]` : Neem het `i` element van `a` , pak het uit en haal vervolgens het element 3e van de niet-ingepakte waarde op (dit moet een matrix zijn).</span><span class="sxs-lookup"><span data-stu-id="484a9-228">`!` and `[]` bind positionally; that is, `a[i]![3]` is read as `((a[i])!)[3]`: take the `i`th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="484a9-229">De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="484a9-229">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="484a9-230">Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.</span><span class="sxs-lookup"><span data-stu-id="484a9-230">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="484a9-231">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="484a9-231">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="484a9-232">Matrix expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-232">Array Expressions</span></span>

<span data-ttu-id="484a9-233">Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen vier Kante haken `[]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-233">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in square brackets `[]`.</span></span>
<span data-ttu-id="484a9-234">Alle elementen moeten compatibel zijn met hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="484a9-234">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="484a9-235">Als er twee matrices van hetzelfde type zijn opgegeven, gebruikt u de binaire `+` operator om een nieuwe matrix te vormen die de samen voeging van de twee matrices vormt.</span><span class="sxs-lookup"><span data-stu-id="484a9-235">Given two arrays of the same type, use the binary `+` operator to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="484a9-236">Bijvoorbeeld `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="484a9-236">For example, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="484a9-237">Matrix maken</span><span class="sxs-lookup"><span data-stu-id="484a9-237">Array Creation</span></span>

<span data-ttu-id="484a9-238">Met een type en een `Int` expressie kunt u de `new` operator gebruiken om een nieuwe matrix met de opgegeven grootte toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="484a9-238">Given a type and an `Int` expression, use the `new` operator to allocate a new array of the given size.</span></span>
<span data-ttu-id="484a9-239">`new Int[i + 1]`Wijst bijvoorbeeld een nieuwe `Int` matrix met `i + 1` elementen toe.</span><span class="sxs-lookup"><span data-stu-id="484a9-239">For example, `new Int[i + 1]` allocates a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="484a9-240">Lege letterlijke arrays, zoals `[]` , zijn niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="484a9-240">Empty array literals, such as `[]`, are not allowed.</span></span>
<span data-ttu-id="484a9-241">In plaats daarvan kunt u een matrix met een lengte van nul maken met `new T[0]` , waarbij `T` een tijdelijke aanduiding voor een geschikt type is.</span><span class="sxs-lookup"><span data-stu-id="484a9-241">Instead, you can create an array of length zero by using `new T[0]`, where `T` is a placeholder for a suitable type.</span></span>

<span data-ttu-id="484a9-242">De elementen van een nieuwe matrix worden geïnitialiseerd naar een type-afhankelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="484a9-242">The elements of a new array initialize to a type-dependent default value.</span></span>
<span data-ttu-id="484a9-243">In de meeste gevallen is dit een variatie van nul.</span><span class="sxs-lookup"><span data-stu-id="484a9-243">In most cases, this is some variation of zero.</span></span>

<span data-ttu-id="484a9-244">Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="484a9-244">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="484a9-245">Voor deze typen is de standaard waarde een ongeldige verwijzing die u niet kunt gebruiken zonder dat er een runtime-fout wordt veroorzaakt, vergelijkbaar met een null-verwijzing in talen als C# of Java.</span><span class="sxs-lookup"><span data-stu-id="484a9-245">Thus, for these types, the default is an invalid reference that you cannot use without causing a runtime error, similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="484a9-246">Matrices met qubits of callables moeten worden geïnitialiseerd met niet-standaard waarden voordat u de elementen ervan veilig kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="484a9-246">Arrays containing qubits or callables must be initialized with non-default values before you can use their elements safely.</span></span> <span data-ttu-id="484a9-247">Zie voor de juiste initialisatie routines <xref:Microsoft.Quantum.Arrays> .</span><span class="sxs-lookup"><span data-stu-id="484a9-247">For suitable initialization routines, see <xref:Microsoft.Quantum.Arrays>.</span></span>

<span data-ttu-id="484a9-248">De standaard waarden voor elk type zijn:</span><span class="sxs-lookup"><span data-stu-id="484a9-248">The default values for each type are:</span></span>

<span data-ttu-id="484a9-249">Type</span><span class="sxs-lookup"><span data-stu-id="484a9-249">Type</span></span> | <span data-ttu-id="484a9-250">Standaard</span><span class="sxs-lookup"><span data-stu-id="484a9-250">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="484a9-251">_Ongeldige Qubit_</span><span class="sxs-lookup"><span data-stu-id="484a9-251">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="484a9-252">Het lege bereik, `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="484a9-252">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="484a9-253">_Ongeldige aanroepable_</span><span class="sxs-lookup"><span data-stu-id="484a9-253">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="484a9-254">Type tuple Initialiseer element-by-element.</span><span class="sxs-lookup"><span data-stu-id="484a9-254">Tuple types initialize element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="484a9-255">Matrix elementen</span><span class="sxs-lookup"><span data-stu-id="484a9-255">Array Elements</span></span>

<span data-ttu-id="484a9-256">Een matrix expressie en een `Int` expressie, vormen een nieuwe expressie met de operator matrix element `[]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-256">Given an array expression and an `Int` expression, form a new expression using the array element operator `[]`.</span></span>
<span data-ttu-id="484a9-257">De nieuwe expressie is van hetzelfde type als het element type van de matrix.</span><span class="sxs-lookup"><span data-stu-id="484a9-257">The new expression is the same type as the element type of the array.</span></span>
<span data-ttu-id="484a9-258">Als bijvoorbeeld `a` is gebonden aan een matrix van het type `Double` , `a[4]` is een `Double` expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-258">For example, if `a` is bound to an array of type `Double`, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="484a9-259">Als de matrix expressie geen eenvoudige id is, moet u deze tussen haakjes plaatsen om een element te selecteren.</span><span class="sxs-lookup"><span data-stu-id="484a9-259">If the array expression is not a simple identifier, you must enclose it in parentheses to select an element.</span></span>
<span data-ttu-id="484a9-260">Als bijvoorbeeld `a` `b` beide matrices van het type zijn `Int` , wordt een element uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="484a9-260">For example, if `a` and `b` are both arrays of type `Int`, an element from the concatenation is expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="484a9-261">Alle matrices in Q# zijn gebaseerd op nul.</span><span class="sxs-lookup"><span data-stu-id="484a9-261">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="484a9-262">Dat wil zeggen, het eerste element van een matrix `a` is altijd `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-262">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="484a9-263">Matrix segmenten</span><span class="sxs-lookup"><span data-stu-id="484a9-263">Array Slices</span></span>

<span data-ttu-id="484a9-264">Een matrix expressie en een `Range` expressie, vormen een nieuwe expressie met de operator matrix segment `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-264">Given an array expression and a `Range` expression, form a new expression using the array slice operator `[ ]`.</span></span>
<span data-ttu-id="484a9-265">De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die zijn geïndexeerd door de elementen van de `Range` , in de volg orde die is gedefinieerd door de `Range` .</span><span class="sxs-lookup"><span data-stu-id="484a9-265">The new expression is the same type as the array and contains the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="484a9-266">Als bijvoorbeeld `a` is gebonden aan een matrix van het type `Double` , `a[3..-1..0]` is `Double[]` dit een expressie die de eerste vier elementen van `a` , maar in de omgekeerde volg orde bevat zoals ze worden weer gegeven in `a` .</span><span class="sxs-lookup"><span data-stu-id="484a9-266">For example, if `a` is bound to an array of type `Double`, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="484a9-267">Als het `Range` leeg is, is het resulterende matrix segment geen lengte van nul.</span><span class="sxs-lookup"><span data-stu-id="484a9-267">If the `Range` is empty, then the resulting array slice is zero length.</span></span>

<span data-ttu-id="484a9-268">Net als bij het verwijzen naar matrix elementen, moet u de matrix expressie tussen haakjes plaatsen om deze te segmenteren.</span><span class="sxs-lookup"><span data-stu-id="484a9-268">Just as with referencing array elements, if the array expression is not a simple identifier, you must enclose it in parentheses to slice it.</span></span>
<span data-ttu-id="484a9-269">Als bijvoorbeeld `a` `b` beide matrices van het type zijn `Int` , wordt een segment uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="484a9-269">For example, if `a` and `b` are both arrays of type `Int`, a slice from the concatenation is expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="484a9-270">Uitgestelde begin-en eind waarden</span><span class="sxs-lookup"><span data-stu-id="484a9-270">Inferred start/end values</span></span>

<span data-ttu-id="484a9-271">Vanaf onze [0,8-release](xref:microsoft.quantum.relnotes)ondersteunen we context afhankelijke expressies voor bereik segmenting.</span><span class="sxs-lookup"><span data-stu-id="484a9-271">Starting with our [0.8 release](xref:microsoft.quantum.relnotes), we support contextual expressions for range slicing.</span></span> <span data-ttu-id="484a9-272">Met name kunt u de begin-en eind waarden van het bereik weglaten in de context van een expressie voor bereik segmentatie.</span><span class="sxs-lookup"><span data-stu-id="484a9-272">In particular, you may omit range start and end values in the context of a range slicing expression.</span></span> <span data-ttu-id="484a9-273">In dat geval past de compiler de volgende regels toe om de beoogde scheidings tekens voor het bereik af te leiden:</span><span class="sxs-lookup"><span data-stu-id="484a9-273">In that case, the compiler applies the following rules to infer the intended delimiters for the range:</span></span>

* <span data-ttu-id="484a9-274">Als de *begin* waarde van het bereik wordt wegge laten, wordt de uitgestelde begin waarde</span><span class="sxs-lookup"><span data-stu-id="484a9-274">If the range *start* value is omitted, then the inferred start value</span></span>
  * <span data-ttu-id="484a9-275">is nul als er geen stap is opgegeven of de opgegeven stap positief is.</span><span class="sxs-lookup"><span data-stu-id="484a9-275">is zero if no step is specified or the specified step is positive.</span></span>  
  * <span data-ttu-id="484a9-276">is de lengte van de gesegmenteerde matrix min één als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="484a9-276">is the length of the sliced array minus one if the specified step is negative.</span></span>

* <span data-ttu-id="484a9-277">Als de *eind* waarde van het bereik wordt wegge laten, wordt de uitgestelde eind waarde</span><span class="sxs-lookup"><span data-stu-id="484a9-277">If the range *end* value is omitted, then the inferred end value</span></span>
  * <span data-ttu-id="484a9-278">is de lengte van de gesegmenteerde matrix min één als er geen stap is opgegeven of de opgegeven stap positief is.</span><span class="sxs-lookup"><span data-stu-id="484a9-278">is the length of the sliced array minus one if no step is specified or the specified step is positive.</span></span>
  * <span data-ttu-id="484a9-279">is nul als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="484a9-279">is zero if the specified step is negative.</span></span>

<span data-ttu-id="484a9-280">Een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="484a9-280">Some examples are:</span></span>

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="484a9-281">Expressies kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="484a9-281">Copy-and-Update Expressions</span></span>

<span data-ttu-id="484a9-282">Aangezien alle Q# typen waarden zijn (waarbij de qubits een enigszins speciale rol neemt), wordt er formeel een ' Copy ' gemaakt wanneer een waarde aan een symbool is gebonden of wanneer een symbool wordt losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="484a9-282">Since all Q# types are value types (with the qubits taking a somewhat special role), formally a "copy" is created when a value is bound to a symbol or when a symbol is rebound.</span></span> <span data-ttu-id="484a9-283">Dat wil zeggen, het gedrag van Q# is hetzelfde als wanneer een kopie is gemaakt met behulp van een toewijzings operator.</span><span class="sxs-lookup"><span data-stu-id="484a9-283">That is to say, the behavior of Q# is the same as if a copy were created using an assignment operator.</span></span> 

<span data-ttu-id="484a9-284">Natuurlijk, in de praktijk, worden alleen de relevante onderdelen opnieuw gemaakt als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="484a9-284">Of course, in practice, only the relevant pieces are recreated as needed.</span></span> <span data-ttu-id="484a9-285">Dit is van invloed op hoe u matrices kopieert, omdat het niet mogelijk is om matrix items bij te werken.</span><span class="sxs-lookup"><span data-stu-id="484a9-285">This affects how you copy arrays because it is not possible to update array items.</span></span> <span data-ttu-id="484a9-286">Voor het wijzigen van een bestaande matrix is een mechanisme voor *kopiëren en bijwerken* vereist.</span><span class="sxs-lookup"><span data-stu-id="484a9-286">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="484a9-287">U kunt een nieuwe matrix maken op basis van een bestaande matrix via de expressies *kopiëren en bijwerken* , die gebruikmaken van de Opera tors `w/` en `<-` .</span><span class="sxs-lookup"><span data-stu-id="484a9-287">You can create a new array from an existing array via *copy-and-update* expressions, which use the operators `w/` and `<-`.</span></span>
<span data-ttu-id="484a9-288">Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3` , waarbij</span><span class="sxs-lookup"><span data-stu-id="484a9-288">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where</span></span>

* <span data-ttu-id="484a9-289">`expression1` moet een type zijn `T[]` voor een bepaald type `T` .</span><span class="sxs-lookup"><span data-stu-id="484a9-289">`expression1` must be type `T[]` for some type `T`.</span></span>
* <span data-ttu-id="484a9-290">`expression2` Hiermee wordt gedefinieerd welke indexen in de opgegeven matrix `expression1` worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="484a9-290">`expression2` defines which indices in the array specified in `expression1` to modify.</span></span> <span data-ttu-id="484a9-291">`expression2` moet van het type `Int` of van een type zijn `Range` .</span><span class="sxs-lookup"><span data-stu-id="484a9-291">`expression2` must be either type `Int` or type `Range`.</span></span>
* <span data-ttu-id="484a9-292">`expression3` is de waarde (n) die wordt gebruikt voor het bijwerken van elementen in `expression1` , op basis van de indices die zijn opgegeven in `expression2` .</span><span class="sxs-lookup"><span data-stu-id="484a9-292">`expression3` is the value(s) used to update elements in `expression1`, based on the indices specified in `expression2`.</span></span> <span data-ttu-id="484a9-293">Als `expression2` is type `Int` , `expression3` moet type zijn `T` .</span><span class="sxs-lookup"><span data-stu-id="484a9-293">If `expression2` is type `Int`, `expression3` must be type `T`.</span></span> <span data-ttu-id="484a9-294">Als `expression2` is type `Range` , `expression3` moet type zijn `T[]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-294">If `expression2` is type `Range`, `expression3` must be type `T[]`.</span></span>

<span data-ttu-id="484a9-295">De expressie Copy-and-update `arr w/ idx <- value` bouwt bijvoorbeeld een nieuwe matrix met alle elementen die zijn ingesteld op de overeenkomstige elementen in `arr` , met uitzonde ring van het element (en) `idx` dat is opgegeven door, die is ingesteld op de waarde (n) in `value` .</span><span class="sxs-lookup"><span data-stu-id="484a9-295">For example, the copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding elements in `arr`, except for the element(s) specified by `idx`, which is set to the value(s) in `value`.</span></span> 

<span data-ttu-id="484a9-296">Opgegeven `arr` bevat de matrix `[0,1,2,3]` en vervolgens</span><span class="sxs-lookup"><span data-stu-id="484a9-296">Given `arr` contains the array `[0,1,2,3]`, then</span></span> 

- <span data-ttu-id="484a9-297">`arr w/ 0 <- 10` is de matrix `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-297">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="484a9-298">`arr w/ 2 <- 10` is de matrix `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-298">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="484a9-299">`arr w/ 0..2..3 <- [10,12]` is de matrix `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-299">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="484a9-300">Expressies kopiëren en bijwerken voor benoemde items</span><span class="sxs-lookup"><span data-stu-id="484a9-300">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="484a9-301">Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="484a9-301">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="484a9-302">Denk bijvoorbeeld aan het type</span><span class="sxs-lookup"><span data-stu-id="484a9-302">For example, consider the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="484a9-303">Als `c` de waarde van het type bevat `Complex(1., -1.)` , `c w/ Re <- 0.` is dit een expressie van het type `Complex` waarmee wordt geëvalueerd `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="484a9-303">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="484a9-304">Gekartelde matrices</span><span class="sxs-lookup"><span data-stu-id="484a9-304">Jagged Arrays</span></span>

<span data-ttu-id="484a9-305">Een gekartelde matrix, ook wel een matrix van matrices genoemd, is een matrix waarvan de elementen matrices zijn.</span><span class="sxs-lookup"><span data-stu-id="484a9-305">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="484a9-306">De elementen van een gekartelde matrix kunnen van verschillende grootten zijn.</span><span class="sxs-lookup"><span data-stu-id="484a9-306">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="484a9-307">In het volgende voor beeld ziet u hoe u een gekartelde matrix die een vermenigvuldigings tabel vertegenwoordigt, declareert en initialiseert.</span><span class="sxs-lookup"><span data-stu-id="484a9-307">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="484a9-308">Matrices van callables</span><span class="sxs-lookup"><span data-stu-id="484a9-308">Arrays of callables</span></span> 

<span data-ttu-id="484a9-309">U kunt ook een matrix van callables maken.</span><span class="sxs-lookup"><span data-stu-id="484a9-309">You can also create an array of callables.</span></span>

* <span data-ttu-id="484a9-310">Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.</span><span class="sxs-lookup"><span data-stu-id="484a9-310">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
* <span data-ttu-id="484a9-311">Het element type van de matrix ondersteunt alle [functors](xref:microsoft.quantum.guide.operationsfunctions) die door alle elementen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="484a9-311">The element type of the array supports any [functors](xref:microsoft.quantum.guide.operationsfunctions) that are supported by all of the elements.</span></span>
<span data-ttu-id="484a9-312">Bijvoorbeeld als `Op1` , `Op2` en `Op3` alle `Qubit[] => Unit` bewerkingen zijn, maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:</span><span class="sxs-lookup"><span data-stu-id="484a9-312">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit` operations, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>
  * <span data-ttu-id="484a9-313">`[Op1, Op2]` is een matrix met `(Qubit[] => Unit)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="484a9-313">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
  * <span data-ttu-id="484a9-314">`[Op1, Op3]` is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="484a9-314">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
  * <span data-ttu-id="484a9-315">`[Op2, Op3]` is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="484a9-315">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="484a9-316">Terwijl de bewerkingen `(Qubit[] => Unit is Adj)` en  `(Qubit[] => Unit is Ctl)` het gebruikelijke basis type van zijn `(Qubit[] => Unit)` , delen *matrices* van deze bewerkingen echter geen gemeen schappelijk basis type.</span><span class="sxs-lookup"><span data-stu-id="484a9-316">However, while the operations `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` have the common base type of `(Qubit[] => Unit)`, *arrays* of these operations do not share a common base type.</span></span>

<span data-ttu-id="484a9-317">Er wordt bijvoorbeeld `[[Op1], [Op2]]` momenteel een fout gegenereerd omdat er wordt geprobeerd een matrix te maken van de twee incompatibele matrix typen `(Qubit[] => Unit is Adj)[]` en `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-317">For example, `[[Op1], [Op2]]` would currently raise an error because it attempts to create an array of the two incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>

<span data-ttu-id="484a9-318">Zie [aanroep bare expressies](#callable-expressions) op deze pagina of [bewerkingen Q# en functies in ](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie over callables.</span><span class="sxs-lookup"><span data-stu-id="484a9-318">For more information on callables, see [Callable expressions](#callable-expressions)  on this page or [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="484a9-319">Voorwaardelijke expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-319">Conditional Expressions</span></span>

<span data-ttu-id="484a9-320">Er zijn twee expressies van hetzelfde type en een booleaanse expressie die een voorwaardelijke expressie vormen met het vraag teken, `?` en de verticale balk `|` .</span><span class="sxs-lookup"><span data-stu-id="484a9-320">Given two expressions of the same type and a Boolean expression, form a conditional expression using the question mark, `?`, and the vertical bar `|`.</span></span> <span data-ttu-id="484a9-321">Gegeven `a==b ? c | d` , is de waarde van de voorwaardelijke expressie `c` als `a==b` waar en `d` als deze False is.</span><span class="sxs-lookup"><span data-stu-id="484a9-321">Given `a==b ? c | d`, the value of the conditional expression is `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="484a9-322">Voorwaardelijke expressies met callables</span><span class="sxs-lookup"><span data-stu-id="484a9-322">Conditional expressions with callables</span></span>

<span data-ttu-id="484a9-323">Voorwaardelijke expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="484a9-323">Conditional expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span> <span data-ttu-id="484a9-324">In dit geval is het type van de voorwaardelijke expressie een bewerking met invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="484a9-324">In this case, the type of the conditional expression is an operation with inputs and outputs that support any functors supported by both expressions.</span></span>
<span data-ttu-id="484a9-325">Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[]=>Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:</span><span class="sxs-lookup"><span data-stu-id="484a9-325">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="484a9-326">`flag ? Op1 | Op2` is een `(Qubit[] => Unit)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="484a9-326">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="484a9-327">`flag ? Op1 | Op3` is een `(Qubit[] => Unit is Adj)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="484a9-327">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="484a9-328">`flag ? Op2 | Op3` is een `(Qubit[] => Unit is Ctl)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="484a9-328">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="484a9-329">Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in de waarde van de aanroep.</span><span class="sxs-lookup"><span data-stu-id="484a9-329">If either of the two possible result expressions include a function or operation call, that call only takes place if that result is the one that is the value of the call.</span></span> <span data-ttu-id="484a9-330">In het geval bijvoorbeeld `a==b ? C(qs) | D(qs)` als `a==b` is waar, wordt de `C` bewerking aangeroepen en als deze ONWAAR is, wordt alleen de `D` bewerking aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="484a9-330">For example, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true, then the `C` operation is invoked, and if it is false then only the `D` operation is invoked.</span></span> <span data-ttu-id="484a9-331">Deze benadering is vergelijkbaar met *kort circuits* in andere talen.</span><span class="sxs-lookup"><span data-stu-id="484a9-331">This approach is similar to *short-circuiting* in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="484a9-332">Aanroep bare expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-332">Callable Expressions</span></span>

<span data-ttu-id="484a9-333">Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.</span><span class="sxs-lookup"><span data-stu-id="484a9-333">A callable literal is the name of an operation or function defined in the compilation scope.</span></span> <span data-ttu-id="484a9-334">Een voor beeld `X` is een letterlijke bewerking die verwijst naar de standaard `X` -bibliotheek bewerking en `Message` is een functie-literal die verwijst naar de `Message` functie standaard bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="484a9-334">For example, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="484a9-335">Als een bewerking de `Adjoint` functor ondersteunt, `Adjoint op` is een bewerkings expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-335">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="484a9-336">Op dezelfde manier geldt dat als de bewerking de `Controlled` functor ondersteunt, `Controlled op` een bewerkings expressie is.</span><span class="sxs-lookup"><span data-stu-id="484a9-336">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="484a9-337">Zie [bewerkings bewerkingen aanroepen](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)voor meer informatie over de typen expressies.</span><span class="sxs-lookup"><span data-stu-id="484a9-337">For more information about the types of these expressions, see [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="484a9-338">Functors ( `Adjoint` en `Controlled` ) binden meer nauw keuriger dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="484a9-338">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[ ]`.</span></span>
<span data-ttu-id="484a9-339">Daarom zijn de volgende allemaal geldig, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="484a9-339">Thus, the following are all valid, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="484a9-340">Met type para meter aanroep bare expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-340">Type-parameterized callable expressions</span></span>

<span data-ttu-id="484a9-341">U kunt een aanroep bare letterlijke waarde gebruiken als een teken reeks, bijvoorbeeld om deze toe te wijzen aan een variabele of door geven aan een andere aanroepable.</span><span class="sxs-lookup"><span data-stu-id="484a9-341">You can use a callable literal as a value, for example, to assign it to a variable or pass it to another callable.</span></span> <span data-ttu-id="484a9-342">Als de aanroepable van het [type para meters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)is, moet u in dit geval de para meters opgeven als onderdeel van de aanroep bare waarde.</span><span class="sxs-lookup"><span data-stu-id="484a9-342">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), you must provide the parameters as part of the callable value.</span></span>

<span data-ttu-id="484a9-343">Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben.</span><span class="sxs-lookup"><span data-stu-id="484a9-343">A callable value cannot have any unspecified type parameters.</span></span> <span data-ttu-id="484a9-344">Als `Fun` is bijvoorbeeld een functie met de hand tekening `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="484a9-344">For example, if `Fun` is a function with the signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="484a9-345">Aanroep bare aanroepende expressies</span><span class="sxs-lookup"><span data-stu-id="484a9-345">Callable Invocation Expressions</span></span>

<span data-ttu-id="484a9-346">Gezien een aanroep bare expressie (bewerking of functie) en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kunt u een aanroep *expressie* vormen door de tuple-expressie toe te voegen aan de aanroep bare expressie.</span><span class="sxs-lookup"><span data-stu-id="484a9-346">Given a callable expression (operation or function) and a tuple expression of the input type of the callable's signature, you can form an *invocation expression* by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="484a9-347">Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.</span><span class="sxs-lookup"><span data-stu-id="484a9-347">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="484a9-348">Als bijvoorbeeld `Op` een bewerking met de hand tekening is `((Int, Qubit) => Double)` , `Op(3, qubit1)` is een expressie van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="484a9-348">For example, if `Op` is an operation with the signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="484a9-349">Op dezelfde manier `Sin` is als een functie met de hand tekening `(Double -> Double)` `Sin(0.1)` een expressie van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="484a9-349">Similarly, if `Sin` is a function with the signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="484a9-350">Ten slotte, als `Builder` een functie met de hand tekening `(Int -> (Int -> Int))` , `Builder(3)` is een functie van `Int` naar `Int` .</span><span class="sxs-lookup"><span data-stu-id="484a9-350">Finally, if `Builder` is a function with the signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from `Int` to `Int`.</span></span>

<span data-ttu-id="484a9-351">Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.</span><span class="sxs-lookup"><span data-stu-id="484a9-351">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="484a9-352">Om het resultaat van aanroepen `Builder` vanuit de vorige alinea te kunnen aanroepen, is de juiste syntaxis:</span><span class="sxs-lookup"><span data-stu-id="484a9-352">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="484a9-353">Wanneer u een aanroepable van een [type para meter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) aanroept, kunt u de werkelijke type parameters tussen punt haken `< >` na de aanroep bare expressie opgeven.</span><span class="sxs-lookup"><span data-stu-id="484a9-353">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, you can specify the actual type parameters within angle brackets `< >` after the callable expression.</span></span>
<span data-ttu-id="484a9-354">Deze actie is doorgaans onnodig wanneer de Q# compiler de daad werkelijke typen afleidt.</span><span class="sxs-lookup"><span data-stu-id="484a9-354">This action is usually unnecessary as the Q# compiler infers the actual types.</span></span>
<span data-ttu-id="484a9-355">Het *is* echter wel vereist voor een [gedeeltelijke toepassing](xref:microsoft.quantum.guide.operationsfunctions#partial-application) als een argument van het type para meter left niet is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="484a9-355">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="484a9-356">Het is ook handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.</span><span class="sxs-lookup"><span data-stu-id="484a9-356">It is also useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="484a9-357">Als u bijvoorbeeld een `Func` hand tekening `('T1, 'T2, 'T1) -> 'T2` `Op1` hebt en `Op2` hand tekening hebt en hand tekening hebt, `(Qubit[] => Unit is Adj)` moet u als het `Op3` `(Qubit[] => Unit)` `Func` `Op1` eerste argument als `Op2` tweede en `Op3` als derde worden aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="484a9-357">For example, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="484a9-358">De type specificatie is vereist omdat `Op3` en `Op1` andere typen hebben, waardoor de compiler dit als dubbel zinnig wordt behandeld zonder de specificatie.</span><span class="sxs-lookup"><span data-stu-id="484a9-358">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="484a9-359">Operator prioriteit</span><span class="sxs-lookup"><span data-stu-id="484a9-359">Operator Precedence</span></span>

* <span data-ttu-id="484a9-360">Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^` .</span><span class="sxs-lookup"><span data-stu-id="484a9-360">All binary operators are right-associative, except for `^`.</span></span>

* <span data-ttu-id="484a9-361">U kunt `[ ]` voor elke operator een binding maken,, voor het segmenteren en indexeren van matrices.</span><span class="sxs-lookup"><span data-stu-id="484a9-361">Brackets, `[ ]`, for array slicing and indexing, bind before any operator.</span></span>

* <span data-ttu-id="484a9-362">De functors `Adjoint` en `Controlled` binding na het indexeren van de matrix, maar vóór alle andere opera tors.</span><span class="sxs-lookup"><span data-stu-id="484a9-362">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

* <span data-ttu-id="484a9-363">Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.</span><span class="sxs-lookup"><span data-stu-id="484a9-363">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="484a9-364">Q# Opera tors in volg orde van prioriteit, van hoog naar laag:</span><span class="sxs-lookup"><span data-stu-id="484a9-364">Q# operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="484a9-365">Operator</span><span class="sxs-lookup"><span data-stu-id="484a9-365">Operator</span></span> | <span data-ttu-id="484a9-366">Ariteit</span><span class="sxs-lookup"><span data-stu-id="484a9-366">Arity</span></span> | <span data-ttu-id="484a9-367">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="484a9-367">Description</span></span> | <span data-ttu-id="484a9-368">Typen operand</span><span class="sxs-lookup"><span data-stu-id="484a9-368">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="484a9-369">Volg `!`</span><span class="sxs-lookup"><span data-stu-id="484a9-369">trailing `!`</span></span> | <span data-ttu-id="484a9-370">Unair</span><span class="sxs-lookup"><span data-stu-id="484a9-370">Unary</span></span> | <span data-ttu-id="484a9-371">Unwrap</span><span class="sxs-lookup"><span data-stu-id="484a9-371">Unwrap</span></span> | <span data-ttu-id="484a9-372">Een door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="484a9-372">Any user-defined type</span></span>
 <span data-ttu-id="484a9-373">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="484a9-373">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="484a9-374">Unair</span><span class="sxs-lookup"><span data-stu-id="484a9-374">Unary</span></span> | <span data-ttu-id="484a9-375">Numerieke, negatieve, bitsgewijze complement, logische negatie</span><span class="sxs-lookup"><span data-stu-id="484a9-375">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="484a9-376">`Int`, `BigInt` of voor, `Double` of voor `-` `Int` `BigInt` `~~~` , `Bool` voor `not`</span><span class="sxs-lookup"><span data-stu-id="484a9-376">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="484a9-377">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-377">Binary</span></span> | <span data-ttu-id="484a9-378">Geheel getal energie</span><span class="sxs-lookup"><span data-stu-id="484a9-378">Integer power</span></span> | <span data-ttu-id="484a9-379">`Int` of `BigInt` voor de basis `Int` voor de exponent</span><span class="sxs-lookup"><span data-stu-id="484a9-379">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="484a9-380">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="484a9-380">`/`, `*`, `%`</span></span> | <span data-ttu-id="484a9-381">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-381">Binary</span></span> | <span data-ttu-id="484a9-382">Deling, vermenigvuldiging, integer modulus</span><span class="sxs-lookup"><span data-stu-id="484a9-382">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="484a9-383">`Int`, `BigInt` of `Double` voor `/` en `*` , `Int` of `BigInt` voor `%`</span><span class="sxs-lookup"><span data-stu-id="484a9-383">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="484a9-384">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="484a9-384">`+`, `-`</span></span> | <span data-ttu-id="484a9-385">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-385">Binary</span></span> | <span data-ttu-id="484a9-386">Toevoeging of teken reeks-en matrix samenvoeging, aftrekken</span><span class="sxs-lookup"><span data-stu-id="484a9-386">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="484a9-387">`Int`, `BigInt` of `Double` , ook `String` of een matrix type voor `+`</span><span class="sxs-lookup"><span data-stu-id="484a9-387">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="484a9-388">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="484a9-388">`<<<`, `>>>`</span></span> | <span data-ttu-id="484a9-389">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-389">Binary</span></span> | <span data-ttu-id="484a9-390">Shift-links, Shift-rechts</span><span class="sxs-lookup"><span data-stu-id="484a9-390">Left shift, right shift</span></span> | <span data-ttu-id="484a9-391">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="484a9-391">`Int` or `BigInt`</span></span>
 <span data-ttu-id="484a9-392">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="484a9-392">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="484a9-393">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-393">Binary</span></span> | <span data-ttu-id="484a9-394">Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="484a9-394">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="484a9-395">`Int`, `BigInt` of `Double`</span><span class="sxs-lookup"><span data-stu-id="484a9-395">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="484a9-396">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="484a9-396">`==`, `!=`</span></span> | <span data-ttu-id="484a9-397">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-397">Binary</span></span> | <span data-ttu-id="484a9-398">gelijk, niet-gelijk-vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="484a9-398">equal, not-equal comparisons</span></span> | <span data-ttu-id="484a9-399">een primitief type</span><span class="sxs-lookup"><span data-stu-id="484a9-399">any primitive type</span></span>
 `&&&` | <span data-ttu-id="484a9-400">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-400">Binary</span></span> | <span data-ttu-id="484a9-401">Bitsgewijze AND</span><span class="sxs-lookup"><span data-stu-id="484a9-401">Bitwise AND</span></span> | <span data-ttu-id="484a9-402">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="484a9-402">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="484a9-403">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-403">Binary</span></span> | <span data-ttu-id="484a9-404">Bitsgewijze XOR</span><span class="sxs-lookup"><span data-stu-id="484a9-404">Bitwise XOR</span></span> | <span data-ttu-id="484a9-405">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="484a9-405">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="484a9-406">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-406">Binary</span></span> | <span data-ttu-id="484a9-407">Bitsgewijze OR</span><span class="sxs-lookup"><span data-stu-id="484a9-407">Bitwise OR</span></span> | <span data-ttu-id="484a9-408">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="484a9-408">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="484a9-409">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-409">Binary</span></span> | <span data-ttu-id="484a9-410">Logische AND</span><span class="sxs-lookup"><span data-stu-id="484a9-410">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="484a9-411">Binair</span><span class="sxs-lookup"><span data-stu-id="484a9-411">Binary</span></span> | <span data-ttu-id="484a9-412">Logische OR</span><span class="sxs-lookup"><span data-stu-id="484a9-412">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="484a9-413">Binair/Ternair</span><span class="sxs-lookup"><span data-stu-id="484a9-413">Binary/Ternary</span></span> | <span data-ttu-id="484a9-414">De operator Range</span><span class="sxs-lookup"><span data-stu-id="484a9-414">Range operator</span></span> | `Int`
 <span data-ttu-id="484a9-415">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="484a9-415">`?` `|`</span></span> | <span data-ttu-id="484a9-416">Ternair</span><span class="sxs-lookup"><span data-stu-id="484a9-416">Ternary</span></span> | <span data-ttu-id="484a9-417">Voorwaardelijk</span><span class="sxs-lookup"><span data-stu-id="484a9-417">Conditional</span></span> | <span data-ttu-id="484a9-418">`Bool` voor de linkerkant</span><span class="sxs-lookup"><span data-stu-id="484a9-418">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="484a9-419">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="484a9-419">`w/` `<-`</span></span> | <span data-ttu-id="484a9-420">Ternair</span><span class="sxs-lookup"><span data-stu-id="484a9-420">Ternary</span></span> | <span data-ttu-id="484a9-421">Kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="484a9-421">Copy-and-update</span></span> | <span data-ttu-id="484a9-422">Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="484a9-422">See [Copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="484a9-423">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="484a9-423">Next steps</span></span>

<span data-ttu-id="484a9-424">Nu u kunt werken met expressies in Q# , gaat u naar [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions) voor meer informatie over het definiëren en aanroepen van bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="484a9-424">Now that you can work with expressions in Q#, move on to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
