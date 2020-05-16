---
title: 'Type-expressies in Q #'
description: 'Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: 93432cef9711b6780192cd59e92b09647a264b5c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431203"
---
# <a name="type-expressions-in-q"></a><span data-ttu-id="36df5-103">Type-expressies in Q #</span><span class="sxs-lookup"><span data-stu-id="36df5-103">Type Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="36df5-104">Numerieke expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-104">Numeric Expressions</span></span>

<span data-ttu-id="36df5-105">Numerieke expressies zijn expressies van het type `Int` , `BigInt` of `Double` .</span><span class="sxs-lookup"><span data-stu-id="36df5-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="36df5-106">Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="36df5-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="36df5-107">`Int`letterlijke waarden in Q # worden eenvoudigweg geschreven als een reeks cijfers.</span><span class="sxs-lookup"><span data-stu-id="36df5-107">`Int` literals in Q# are written simply as a sequence of digits.</span></span>
<span data-ttu-id="36df5-108">Hexadecimale en binaire gehele getallen worden ondersteund met `0x` respectievelijk een en `0b` -voor voegsel.</span><span class="sxs-lookup"><span data-stu-id="36df5-108">Hexadecimal and binary integers are supported with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="36df5-109">`BigInt`letterlijke waarden in Q # worden geschreven met een afsluitend `l` of `L` achtervoegsel.</span><span class="sxs-lookup"><span data-stu-id="36df5-109">`BigInt` literals in Q# are written with a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="36df5-110">Hexadecimale Big-gehele getallen worden ondersteund met het voor voegsel 0x.</span><span class="sxs-lookup"><span data-stu-id="36df5-110">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="36df5-111">Daarom zijn de volgende geldige toepassingen van `BigInt` letterlijke waarden:</span><span class="sxs-lookup"><span data-stu-id="36df5-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="36df5-112">`Double`letterlijke waarden in Q # zijn drijvende-komma getallen die zijn geschreven met decimale cijfers.</span><span class="sxs-lookup"><span data-stu-id="36df5-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="36df5-113">Ze kunnen worden geschreven met een decimaal teken, `.` en/of een exponentieel onderdeel dat is aangegeven met e of e (waarna alleen een mogelijk minteken en decimaal tekens geldig zijn).</span><span class="sxs-lookup"><span data-stu-id="36df5-113">They can be written with a decimal point, `.`, and/or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="36df5-114">Hier volgen geldige `Double` letterlijke waarden: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="36df5-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="36df5-115">Een expressie met een matrix expressie van elk element type `Int` kan worden gevormd met behulp van de [`Length`](xref:microsoft.quantum.core.length) ingebouwde functie, met de matrix expressie tussen haakjes `(` en `)` .</span><span class="sxs-lookup"><span data-stu-id="36df5-115">Given an array expression of any element type, an `Int` expression may be formed using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="36df5-116">Als bijvoorbeeld `a` is gebonden aan een matrix, `Length(a)` is dit een expressie met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="36df5-116">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="36df5-117">Als `b` is een matrix met matrices van gehele getallen, `Int[][]` `Length(b)` is dit het aantal submatrixen in `b` en `Length(b[1])` is het aantal gehele getallen in de tweede submatrix in `b` .</span><span class="sxs-lookup"><span data-stu-id="36df5-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="36df5-118">Gegeven twee numerieke expressies van hetzelfde type, de binaire Opera tors `+` , `-` , `*` en `/` kunnen worden gebruikt om een nieuwe numerieke expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="36df5-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="36df5-119">Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.</span><span class="sxs-lookup"><span data-stu-id="36df5-119">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="36df5-120">Als u twee geheeltallige expressies hebt opgegeven, kan de binaire operator `^` (Power) worden gebruikt voor het maken van een nieuwe expressie met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="36df5-120">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="36df5-121">Dit `^` kan ook worden gebruikt met twee dubbele expressies om een nieuwe dubbele expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="36df5-121">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="36df5-122">Ten slotte `^` kan worden gebruikt met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant om een nieuwe Big Integer-expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="36df5-122">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="36df5-123">In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="36df5-123">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="36df5-124">Als er twee integere of Big Integer-expressies zijn opgegeven, kan een nieuwe integer of Big Integer-expressie worden gevormd met behulp van de `%` Opera tors (modulus), `&&&` (bitsgewijze en), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR).</span><span class="sxs-lookup"><span data-stu-id="36df5-124">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="36df5-125">Geef een geheel getal of een Big Integer-expressie aan de linkerkant en een expressie met gehele getallen aan de rechter kant, de `<<<` (reken kundige Shift-toets links) of de `>>>` Opera tors reken kundig naar rechts kan worden gebruikt om een nieuwe expressie te maken met hetzelfde type als de linker expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-125">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="36df5-126">De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="36df5-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="36df5-127">Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="36df5-127">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="36df5-128">Als het getal dat moet worden verplaatst een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64` ; dat wil zeggen, een verschuiving van 1 en een verschuiving van 65 hebben hetzelfde effect.</span><span class="sxs-lookup"><span data-stu-id="36df5-128">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="36df5-129">Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.</span><span class="sxs-lookup"><span data-stu-id="36df5-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="36df5-130">Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.</span><span class="sxs-lookup"><span data-stu-id="36df5-130">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="36df5-131">Dat wil zeggen dat de ene stap naar links of rechts verschuift precies hetzelfde is als vermenigvuldigen of delen met 2.</span><span class="sxs-lookup"><span data-stu-id="36df5-131">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="36df5-132">Geheel getal delen en integers modulus volgen hetzelfde gedrag voor negatieve getallen als C#.</span><span class="sxs-lookup"><span data-stu-id="36df5-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="36df5-133">Dat wil zeggen, heeft `a % b` altijd hetzelfde teken als `a` en is `b * (a / b) + a % b` altijd gelijk aan `a` .</span><span class="sxs-lookup"><span data-stu-id="36df5-133">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="36df5-134">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="36df5-134">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="36df5-135">5</span><span class="sxs-lookup"><span data-stu-id="36df5-135">5</span></span> | <span data-ttu-id="36df5-136">2</span><span class="sxs-lookup"><span data-stu-id="36df5-136">2</span></span> | <span data-ttu-id="36df5-137">2</span><span class="sxs-lookup"><span data-stu-id="36df5-137">2</span></span> | <span data-ttu-id="36df5-138">1</span><span class="sxs-lookup"><span data-stu-id="36df5-138">1</span></span>
 <span data-ttu-id="36df5-139">5</span><span class="sxs-lookup"><span data-stu-id="36df5-139">5</span></span> | <span data-ttu-id="36df5-140">-2</span><span class="sxs-lookup"><span data-stu-id="36df5-140">-2</span></span> | <span data-ttu-id="36df5-141">-2</span><span class="sxs-lookup"><span data-stu-id="36df5-141">-2</span></span> | <span data-ttu-id="36df5-142">1</span><span class="sxs-lookup"><span data-stu-id="36df5-142">1</span></span>
 <span data-ttu-id="36df5-143">5</span><span class="sxs-lookup"><span data-stu-id="36df5-143">-5</span></span> | <span data-ttu-id="36df5-144">2</span><span class="sxs-lookup"><span data-stu-id="36df5-144">2</span></span> | <span data-ttu-id="36df5-145">-2</span><span class="sxs-lookup"><span data-stu-id="36df5-145">-2</span></span> | <span data-ttu-id="36df5-146">-1</span><span class="sxs-lookup"><span data-stu-id="36df5-146">-1</span></span>
 <span data-ttu-id="36df5-147">5</span><span class="sxs-lookup"><span data-stu-id="36df5-147">-5</span></span> | <span data-ttu-id="36df5-148">-2</span><span class="sxs-lookup"><span data-stu-id="36df5-148">-2</span></span> | <span data-ttu-id="36df5-149">2</span><span class="sxs-lookup"><span data-stu-id="36df5-149">2</span></span> | <span data-ttu-id="36df5-150">-1</span><span class="sxs-lookup"><span data-stu-id="36df5-150">-1</span></span>

<span data-ttu-id="36df5-151">Het delen van een groot geheel getal en modulus werkt op dezelfde manier.</span><span class="sxs-lookup"><span data-stu-id="36df5-151">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="36df5-152">Op basis van een numerieke expressie kan een nieuwe expressie worden gevormd met behulp van de `-` unaire operator.</span><span class="sxs-lookup"><span data-stu-id="36df5-152">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="36df5-153">De nieuwe expressie is van hetzelfde type als de component-expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-153">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="36df5-154">Een nieuwe expressie van hetzelfde type als een geheel getal of Big Integer-expressie kan worden gevormd met behulp van de `~~~` (bitsgewijze complement) monadische operator.</span><span class="sxs-lookup"><span data-stu-id="36df5-154">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="36df5-155">Booleaanse expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-155">Boolean Expressions</span></span>

<span data-ttu-id="36df5-156">De twee `Bool` letterlijke waarden zijn `true` en `false` .</span><span class="sxs-lookup"><span data-stu-id="36df5-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="36df5-157">Op basis van twee expressies van hetzelfde primitieve type `==` kunnen de en `!=` binaire Opera tors worden gebruikt voor het maken van een `Bool` expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="36df5-158">De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.</span><span class="sxs-lookup"><span data-stu-id="36df5-158">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="36df5-159">Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="36df5-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="36df5-160">Als u bijvoorbeeld de operator ' uitpakken ' gebruikt `!` (in detail beschreven bij [typen in Q #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span><span class="sxs-lookup"><span data-stu-id="36df5-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="36df5-161">Gelijkheids vergelijking voor `Qubit` waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.</span><span class="sxs-lookup"><span data-stu-id="36df5-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="36df5-162">De status van de twee qubits wordt niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.</span><span class="sxs-lookup"><span data-stu-id="36df5-162">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="36df5-163">Gelijkheids vergelijking voor `Double` waarden kan misleiden door Afrondings effecten.</span><span class="sxs-lookup"><span data-stu-id="36df5-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="36df5-164">Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="36df5-164">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="36df5-165">Met een wille keurige combi natie van twee numerieke expressies worden de binaire Opera tors `>` ,, `<` `>=` en `<=` kunnen worden gebruikt om een nieuwe booleaanse expressie te maken die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="36df5-166">Aan de hand van twee Booleaanse expressies `and` kunnen de en `or` binaire Opera tors worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als beide (of beide) de twee expressies waar zijn.</span><span class="sxs-lookup"><span data-stu-id="36df5-166">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="36df5-167">Aan de hand van een booleaanse expressie `not` kan de unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.</span><span class="sxs-lookup"><span data-stu-id="36df5-167">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="36df5-168">Teken reeks expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-168">String Expressions</span></span>

<span data-ttu-id="36df5-169">Q # Hiermee kunnen teken reeksen worden gebruikt in de `fail` instructie (toegelicht bij [controle stroom](xref:microsoft.quantum.guide.controlflow#fail-statement)) en in de [`Message`](xref:microsoft.quantum.intrinsic.message) standaard functie.</span><span class="sxs-lookup"><span data-stu-id="36df5-169">Q# allows strings to be used in the `fail` statement (explained at [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span>
<span data-ttu-id="36df5-170">Het specifieke gedrag van de laatste is afhankelijk van de gebruikte simulator, maar schrijft meestal een bericht naar de host-console wanneer het wordt aangeroepen tijdens een Q #-programma.</span><span class="sxs-lookup"><span data-stu-id="36df5-170">The specific behavior of the latter depends on the simulator being used, but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="36df5-171">Teken reeksen in Q # zijn letterlijke waarden of geïnterpoleerde teken reeksen.</span><span class="sxs-lookup"><span data-stu-id="36df5-171">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="36df5-172">Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks van Unicode-tekens tussen dubbele citaten, `"` .</span><span class="sxs-lookup"><span data-stu-id="36df5-172">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="36df5-173">In een teken reeks kan de back slash-teken `\` worden gebruikt om een dubbel aanhalings teken te escapen en om een nieuwe regel als een regel `\n` terugloop als en een tab in te voegen als `\r` `\t` .</span><span class="sxs-lookup"><span data-stu-id="36df5-173">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="36df5-174">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="36df5-174">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="36df5-175">Geïnterpoleerde teken reeksen</span><span class="sxs-lookup"><span data-stu-id="36df5-175">Interpolated strings</span></span>

<span data-ttu-id="36df5-176">De syntaxis van Q # voor teken reeks-interpolatie is een subset van de C#-syntaxis, maar hier worden de belangrijkste punten voor Q # samenvatten.</span><span class="sxs-lookup"><span data-stu-id="36df5-176">The Q# syntax for string interpolations is a subset of the C# syntax, but we summarize here the key points as they pertain to Q#.</span></span>
<span data-ttu-id="36df5-177">De belangrijkste verschillen worden hieronder besproken.</span><span class="sxs-lookup"><span data-stu-id="36df5-177">The main distinctions are discussed below.</span></span>

<span data-ttu-id="36df5-178">Als u een letterlijke teken reeks als een geïnterpoleerde teken reeks wilt identificeren, laten voorafgaan door u deze met het `$` symbool.</span><span class="sxs-lookup"><span data-stu-id="36df5-178">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span>
<span data-ttu-id="36df5-179">Er mag geen spatie staan tussen de `$` en `"` die een letterlijke teken reeks start.</span><span class="sxs-lookup"><span data-stu-id="36df5-179">You cannot have any white space between the `$`and the `"` that starts a string literal.</span></span>

<span data-ttu-id="36df5-180">Hier volgt een voor beeld van een basis voorbeeld waarin de functie wordt gebruikt [`Message`](xref:microsoft.quantum.intrinsic.message) om het resultaat van een meting te schrijven naar de-console, naast andere Q #-expressies.</span><span class="sxs-lookup"><span data-stu-id="36df5-180">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
<span data-ttu-id="36df5-181">Een geldige Q #-expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.</span><span class="sxs-lookup"><span data-stu-id="36df5-181">Any valid Q# expression may appear in an interpolated string.</span></span>

<span data-ttu-id="36df5-182">Meer informatie over de C#-syntaxis vindt u in [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="36df5-182">Further details on the C# syntax can be found at [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>
<span data-ttu-id="36df5-183">Het belangrijkste verschil is dat Q # geen Verbatim-geïnterpoleerde teken reeksen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="36df5-183">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="36df5-184">Expressies binnen een geïnterpoleerde teken reeks volgen Q # syntaxis, geen C#-syntaxis.</span><span class="sxs-lookup"><span data-stu-id="36df5-184">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="36df5-185">Bereik expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-185">Range Expressions</span></span>

<span data-ttu-id="36df5-186">Er zijn drie `Int` expressies `start` , `step` en, `stop` `start .. step .. stop` een bereik expressie waarvan het eerste element, het tweede element, het derde element is `start` `start+step` `start+step+step` , enzovoort, totdat het `stop` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="36df5-186">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="36df5-187">Een bereik kan leeg zijn als bijvoorbeeld `step` positief is en `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="36df5-187">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="36df5-188">Het laatste element van het bereik is `stop` het verschil tussen `start` en `stop` is een integraal veelvoud van `step` ; dat wil zeggen, het bereik is op beide uiteinden.</span><span class="sxs-lookup"><span data-stu-id="36df5-188">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="36df5-189">`Int`Als u twee expressies opgeeft `start` en `stop` , `start .. stop` is dit een bereik expressie die gelijk is aan `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="36df5-189">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="36df5-190">Houd er rekening mee dat de geïmpliceerde `step` is + 1, zelfs als `stop` deze kleiner is dan `start` ; in dit geval is het bereik leeg.</span><span class="sxs-lookup"><span data-stu-id="36df5-190">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="36df5-191">Enkele voor beelden van bereiken:</span><span class="sxs-lookup"><span data-stu-id="36df5-191">Some example ranges are:</span></span>

- <span data-ttu-id="36df5-192">`1..3`is het bereik van 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="36df5-192">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="36df5-193">`2..2..5`is het bereik van 2, 4.</span><span class="sxs-lookup"><span data-stu-id="36df5-193">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="36df5-194">`2..2..6`is het bereik 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="36df5-194">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="36df5-195">`6..-2..2`is het bereik van 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="36df5-195">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="36df5-196">`2..1`is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="36df5-196">`2..1` is the empty range.</span></span>
- <span data-ttu-id="36df5-197">`2..6..7`is het bereik 2.</span><span class="sxs-lookup"><span data-stu-id="36df5-197">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="36df5-198">`2..2..1`is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="36df5-198">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="36df5-199">`1..-1..2`is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="36df5-199">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="36df5-200">Qubit-expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-200">Qubit Expressions</span></span>

<span data-ttu-id="36df5-201">De enige `Qubit` expressies zijn symbolen die zijn gebonden aan `Qubit` waarden of matrix elementen van `Qubit` matrices.</span><span class="sxs-lookup"><span data-stu-id="36df5-201">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="36df5-202">Er zijn geen `Qubit` letterlijke waarden.</span><span class="sxs-lookup"><span data-stu-id="36df5-202">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="36df5-203">Pauli-expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-203">Pauli Expressions</span></span>

<span data-ttu-id="36df5-204">De vier `Pauli` waarden, `PauliI` , `PauliX` , `PauliY` en `PauliZ` zijn allemaal geldige `Pauli` expressies.</span><span class="sxs-lookup"><span data-stu-id="36df5-204">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="36df5-205">Behalve dat zijn de enige `Pauli` expressies symbolen die zijn gebonden aan `Pauli` waarden of matrix elementen van `Pauli` matrices.</span><span class="sxs-lookup"><span data-stu-id="36df5-205">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="36df5-206">Resultaat expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-206">Result Expressions</span></span>

<span data-ttu-id="36df5-207">De twee `Result` waarden `One` en `Zero` zijn geldige `Result` expressies.</span><span class="sxs-lookup"><span data-stu-id="36df5-207">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="36df5-208">Behalve dat zijn de enige `Result` expressies symbolen die zijn gebonden aan `Result` waarden of matrix elementen van `Result` matrices.</span><span class="sxs-lookup"><span data-stu-id="36df5-208">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="36df5-209">Let er met name op dat `One` niet hetzelfde is als het gehele getal `1` en er geen rechtstreekse conversie tussen deze waarden is.</span><span class="sxs-lookup"><span data-stu-id="36df5-209">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="36df5-210">Hetzelfde geldt voor `Zero` en `0` .</span><span class="sxs-lookup"><span data-stu-id="36df5-210">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="36df5-211">Tuple-expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-211">Tuple Expressions</span></span>

<span data-ttu-id="36df5-212">Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen `(` en `)` .</span><span class="sxs-lookup"><span data-stu-id="36df5-212">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="36df5-213">Bijvoorbeeld: `(1, One)` is een `(Int, Result)` expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-213">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="36df5-214">Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.</span><span class="sxs-lookup"><span data-stu-id="36df5-214">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="36df5-215">Door de gebruiker gedefinieerde type expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-215">User-Defined Type Expressions</span></span>

<span data-ttu-id="36df5-216">Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.</span><span class="sxs-lookup"><span data-stu-id="36df5-216">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="36df5-217">Als bijvoorbeeld een door `IntPair` de gebruiker gedefinieerd type is op basis van `(Int, Int)` , is `IntPair(2, 3)` dit een geldige letterlijke waarde van dat type.</span><span class="sxs-lookup"><span data-stu-id="36df5-217">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="36df5-218">Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.</span><span class="sxs-lookup"><span data-stu-id="36df5-218">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="36df5-219">Onverpakte expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-219">Unwrap Expressions</span></span>

<span data-ttu-id="36df5-220">In Q # is de operator voor uitpakken een afsluitend uitroep teken `!` .</span><span class="sxs-lookup"><span data-stu-id="36df5-220">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="36df5-221">Zo `IntPair` is bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `(Int, Int)` en was dit `s` een variabele met de waarde `IntPair(2, 3)` `s!` . vervolgens zou het zijn `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="36df5-221">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2, 3)`, then `s!` would be `(2, 3)`.</span></span>

<span data-ttu-id="36df5-222">Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="36df5-222">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="36df5-223">de operator voor uitpakken kan worden herhaald. `s!!`Hiermee geeft u bijvoorbeeld de dubbele waarde onverpakt van op `s` .</span><span class="sxs-lookup"><span data-stu-id="36df5-223">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="36df5-224">Als is dus `WrappedPair` een door de gebruiker gedefinieerd type met een onderliggend type `IntPair` en dit `t` is een variabele met de waarde `WrappedPair(IntPair(1,2))` , dan `t!!` zou `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="36df5-224">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="36df5-225">De `!` operator heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.</span><span class="sxs-lookup"><span data-stu-id="36df5-225">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="36df5-226">`!`en `[]` positioneel binden; dat wil zeggen, `a[i]![3]` moet worden gelezen als `((a[i])!)[3]` : Neem het `i` element van de th, pak het uit `a` en haal vervolgens het derde element van de niet-ingepakte waarde op (dit moet een matrix zijn).</span><span class="sxs-lookup"><span data-stu-id="36df5-226">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="36df5-227">De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="36df5-227">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="36df5-228">Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.</span><span class="sxs-lookup"><span data-stu-id="36df5-228">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="36df5-229">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="36df5-229">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="36df5-230">Matrix expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-230">Array Expressions</span></span>

<span data-ttu-id="36df5-231">Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen `[` en `]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-231">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="36df5-232">Alle elementen moeten compatibel zijn met hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="36df5-232">All elements must be compatible with the same type.</span></span>


<span data-ttu-id="36df5-233">Als er twee matrices van hetzelfde type zijn opgegeven, kan de binaire `+` operator worden gebruikt voor het vormen van een nieuwe matrix die de samen voeging van de twee matrices vormt.</span><span class="sxs-lookup"><span data-stu-id="36df5-233">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="36df5-234">Bijvoorbeeld: `[1,2,3] + [4,5,6]` `[1,2,3,4,5,6]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-234">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="36df5-235">Matrix maken</span><span class="sxs-lookup"><span data-stu-id="36df5-235">Array Creation</span></span>

<span data-ttu-id="36df5-236">Op basis van een type en een `Int` expressie `new` kan de operator worden gebruikt voor het toewijzen van een nieuwe matrix met de opgegeven grootte.</span><span class="sxs-lookup"><span data-stu-id="36df5-236">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="36df5-237">Bijvoorbeeld, `new Int[i + 1]` zou een nieuwe `Int` matrix met elementen kunnen toewijzen `i + 1` .</span><span class="sxs-lookup"><span data-stu-id="36df5-237">For instance, `new Int[i + 1]` would allocate a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="36df5-238">De elementen van een nieuwe matrix worden geïnitialiseerd op een type-afhankelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="36df5-238">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="36df5-239">In de meeste gevallen is dit een bepaalde variatie van nul.</span><span class="sxs-lookup"><span data-stu-id="36df5-239">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="36df5-240">Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="36df5-240">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="36df5-241">Daarom is de standaard waarde voor deze typen een ongeldige verwijzing die niet kan worden gebruikt zonder dat er een runtime-fout wordt veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="36df5-241">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="36df5-242">Dit is vergelijkbaar met een null-verwijzing in talen als C# of Java.</span><span class="sxs-lookup"><span data-stu-id="36df5-242">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="36df5-243">Matrices met qubits of callables moeten correct worden geïnitialiseerd met niet-standaard waarden voordat de elementen veilig kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="36df5-243">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="36df5-244">Geschikte initialisatie routines kunt u vinden in <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="36df5-244">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="36df5-245">De standaard waarden voor elk type zijn:</span><span class="sxs-lookup"><span data-stu-id="36df5-245">The default values for each type are:</span></span>

<span data-ttu-id="36df5-246">Type</span><span class="sxs-lookup"><span data-stu-id="36df5-246">Type</span></span> | <span data-ttu-id="36df5-247">Standaard</span><span class="sxs-lookup"><span data-stu-id="36df5-247">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="36df5-248">_Ongeldige Qubit_</span><span class="sxs-lookup"><span data-stu-id="36df5-248">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="36df5-249">Het lege bereik,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="36df5-249">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="36df5-250">_Ongeldige aanroepable_</span><span class="sxs-lookup"><span data-stu-id="36df5-250">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="36df5-251">De tuple-typen zijn geïnitialiseerd met element-by-element.</span><span class="sxs-lookup"><span data-stu-id="36df5-251">Tuple types are initialized element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="36df5-252">Matrix elementen</span><span class="sxs-lookup"><span data-stu-id="36df5-252">Array Elements</span></span>

<span data-ttu-id="36df5-253">Met een matrix expressie en een `Int` expressie kan een nieuwe expressie worden gevormd met de `[` operator and van het `]` matrix element.</span><span class="sxs-lookup"><span data-stu-id="36df5-253">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="36df5-254">De nieuwe expressie is van hetzelfde type als het element type van de matrix.</span><span class="sxs-lookup"><span data-stu-id="36df5-254">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="36df5-255">Als bijvoorbeeld `a` is gebonden aan een matrix van `Double` s, dan `a[4]` is een `Double` expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-255">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="36df5-256">Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om een element te selecteren.</span><span class="sxs-lookup"><span data-stu-id="36df5-256">If the array expression is not a simple identifier, it must be enclosed in parentheses in order to select an element.</span></span>
<span data-ttu-id="36df5-257">Als bijvoorbeeld `a` `b` beide matrices van `Int` s zijn, wordt een element uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="36df5-257">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="36df5-258">Alle matrices in Q # zijn gebaseerd op nul.</span><span class="sxs-lookup"><span data-stu-id="36df5-258">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="36df5-259">Dat wil zeggen, het eerste element van een matrix `a` is altijd `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-259">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="36df5-260">Matrix segmenten</span><span class="sxs-lookup"><span data-stu-id="36df5-260">Array Slices</span></span>

<span data-ttu-id="36df5-261">Met een matrix expressie en een `Range` expressie kan een nieuwe expressie worden gevormd met behulp van de `[` operator en de `]` matrix segment.</span><span class="sxs-lookup"><span data-stu-id="36df5-261">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="36df5-262">De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die worden geïndexeerd door de elementen van de `Range` , in de volg orde die is gedefinieerd door de `Range` .</span><span class="sxs-lookup"><span data-stu-id="36df5-262">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="36df5-263">Als bijvoorbeeld `a` is gebonden aan een matrix van `Double` s, `a[3..-1..0]` is `Double[]` dit een expressie die de eerste vier elementen van `a` , maar in de omgekeerde volg orde bevat zoals ze worden weer gegeven in `a` .</span><span class="sxs-lookup"><span data-stu-id="36df5-263">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="36df5-264">Als het `Range` leeg is, is het resulterende matrix segment nul lengte.</span><span class="sxs-lookup"><span data-stu-id="36df5-264">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="36df5-265">Net als bij het verwijzen naar matrix elementen als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om te kunnen worden gesegmenteerd.</span><span class="sxs-lookup"><span data-stu-id="36df5-265">Just as with referencing array elements, if the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="36df5-266">Als `a` en `b` beide matrices van `Int` s, wordt een segment uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="36df5-266">If `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="36df5-267">Uitgestelde begin-en eind waarden</span><span class="sxs-lookup"><span data-stu-id="36df5-267">Inferred start/end values</span></span>

<span data-ttu-id="36df5-268">Vanaf onze 0,8-release ondersteunen we context afhankelijke expressies voor bereik segmenting.</span><span class="sxs-lookup"><span data-stu-id="36df5-268">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="36df5-269">Met name bereik begin-en eind waarden kunnen worden wegge laten in de context van een expressie voor bereik segmentering.</span><span class="sxs-lookup"><span data-stu-id="36df5-269">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="36df5-270">In dat geval past de compiler de volgende regels toe om de beoogde scheidings tekens voor het bereik af te leiden.</span><span class="sxs-lookup"><span data-stu-id="36df5-270">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="36df5-271">Als de begin waarde van het bereik bijvoorbeeld wordt wegge laten, wordt de uitgestelde begin waarde</span><span class="sxs-lookup"><span data-stu-id="36df5-271">For example, if the range start value is omitted,  then the inferred start value</span></span> 
- <span data-ttu-id="36df5-272">is nul als er geen stap is opgegeven of als de opgegeven stap positief is en</span><span class="sxs-lookup"><span data-stu-id="36df5-272">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="36df5-273">is de lengte van de gesegmenteerde matrix min één als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="36df5-273">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="36df5-274">Als de eind waarde van het bereik wordt wegge laten, wordt de uitgestelde eind waarde</span><span class="sxs-lookup"><span data-stu-id="36df5-274">If the range end value is omitted,  then the inferred end value</span></span> 
- <span data-ttu-id="36df5-275">is de lengte van de gesegmenteerde matrix min één als er geen stap is opgegeven, of als de opgegeven stap positief is en</span><span class="sxs-lookup"><span data-stu-id="36df5-275">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="36df5-276">is nul als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="36df5-276">is zero if the specified step is negative.</span></span> 

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="36df5-277">Expressies kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="36df5-277">Copy-and-Update Expressions</span></span>

<span data-ttu-id="36df5-278">Omdat alle typen Q # waardetypen zijn, waarbij de qubits een enigszins speciale rol neemt, wordt formeel een ' Copy ' gemaakt wanneer een waarde is gebonden aan een symbool of wanneer een symbool wordt losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="36df5-278">Since all Q# types are value types — with the qubits taking a somewhat special role —formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="36df5-279">Dat wil zeggen dat het gedrag van Q # hetzelfde is als wanneer er een kopie is gemaakt voor de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="36df5-279">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span>
<span data-ttu-id="36df5-280">Natuurlijk worden alleen de relevante onderdelen, indien nodig, feitelijk opnieuw gemaakt.</span><span class="sxs-lookup"><span data-stu-id="36df5-280">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

<span data-ttu-id="36df5-281">Dit bevat met name ook matrices.</span><span class="sxs-lookup"><span data-stu-id="36df5-281">This in particular also includes arrays.</span></span>
<span data-ttu-id="36df5-282">Met name het is niet mogelijk om matrix items bij te werken.</span><span class="sxs-lookup"><span data-stu-id="36df5-282">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="36df5-283">Voor het wijzigen van een bestaande matrix is een mechanisme voor *kopiëren en bijwerken* vereist.</span><span class="sxs-lookup"><span data-stu-id="36df5-283">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="36df5-284">Nieuwe matrices kunnen worden gemaakt op basis van bestaande met behulp van *Copy-en-update-* expressies.</span><span class="sxs-lookup"><span data-stu-id="36df5-284">New arrays can be created from existing ones via *copy-and-update* expressions.</span></span>
<span data-ttu-id="36df5-285">Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3` , waarbij `expression1` type `T[]` voor een type is `T` .</span><span class="sxs-lookup"><span data-stu-id="36df5-285">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span>
<span data-ttu-id="36df5-286">De tweede `expression2` definieert de indices van de element (en) die moeten worden gewijzigd vergeleken met de matrix in en moet van het type `expression1` `Int` of van het type zijn `Range` .</span><span class="sxs-lookup"><span data-stu-id="36df5-286">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span>
<span data-ttu-id="36df5-287">Als `expression2` is van `Int` het type, moet `expression3` van het type zijn `T` .</span><span class="sxs-lookup"><span data-stu-id="36df5-287">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="36df5-288">Als `expression2` is van `Range` het type, moet `expression3` van het type zijn `T[]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-288">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="36df5-289">Met een copy-and-update-expressie wordt `arr w/ idx <- value` een nieuwe matrix gemaakt met alle elementen die zijn ingesteld op het overeenkomstige element in `arr` , met uitzonde ring van het element (en) op `idx` , die zijn ingesteld op een of meer in `value` .</span><span class="sxs-lookup"><span data-stu-id="36df5-289">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="36df5-290">Als bijvoorbeeld `arr` een matrix bevat `[0,1,2,3]` ,</span><span class="sxs-lookup"><span data-stu-id="36df5-290">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="36df5-291">`arr w/ 0 <- 10`is de matrix `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-291">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="36df5-292">`arr w/ 2 <- 10`is de matrix `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-292">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="36df5-293">`arr w/ 0..2..3 <- [10,12]`is de matrix `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="36df5-293">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="36df5-294">Expressies kopiëren en bijwerken voor benoemde items</span><span class="sxs-lookup"><span data-stu-id="36df5-294">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="36df5-295">Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="36df5-295">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="36df5-296">Denk bijvoorbeeld aan het type</span><span class="sxs-lookup"><span data-stu-id="36df5-296">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="36df5-297">Als `c` de waarde van het type bevat `Complex(1., -1.)` , `c w/ Re <- 0.` is dit een expressie van het type `Complex` waarmee wordt geëvalueerd `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="36df5-297">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="36df5-298">Gekartelde matrices</span><span class="sxs-lookup"><span data-stu-id="36df5-298">Jagged Arrays</span></span>

<span data-ttu-id="36df5-299">Een gekartelde matrix, ook wel een matrix van matrices genoemd, is een matrix waarvan de elementen matrices zijn.</span><span class="sxs-lookup"><span data-stu-id="36df5-299">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="36df5-300">De elementen van een gekartelde matrix kunnen van verschillende grootten zijn.</span><span class="sxs-lookup"><span data-stu-id="36df5-300">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="36df5-301">In het volgende voor beeld ziet u hoe u een gekartelde matrix die een vermenigvuldigings tabel vertegenwoordigt, declareert en initialiseert.</span><span class="sxs-lookup"><span data-stu-id="36df5-301">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="36df5-302">Matrices van callables</span><span class="sxs-lookup"><span data-stu-id="36df5-302">Arrays of callables</span></span> 

<span data-ttu-id="36df5-303">Meer informatie over oproep bare typen vindt u hieronder en op de volgende pagina, [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="36df5-303">Note that more details on callable types can be found below, as well as on the next page, [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

<span data-ttu-id="36df5-304">Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.</span><span class="sxs-lookup"><span data-stu-id="36df5-304">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="36df5-305">Het element type van de matrix ondersteunt alle functors die door alle elementen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="36df5-305">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="36df5-306">Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[] => Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:</span><span class="sxs-lookup"><span data-stu-id="36df5-306">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="36df5-307">`[Op1, Op2]`is een matrix met `(Qubit[] => Unit)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="36df5-307">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="36df5-308">`[Op1, Op3]`is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="36df5-308">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="36df5-309">`[Op2, Op3]`is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="36df5-309">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="36df5-310">Lege letterlijke arrays, `[]` , zijn niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="36df5-310">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="36df5-311">In plaats daarvan `new ★[0]` kunt u, waar `★` als tijdelijke aanduiding voor een geschikt type, de gewenste matrix met een lengte van nul maken.</span><span class="sxs-lookup"><span data-stu-id="36df5-311">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>


## <a name="conditional-expressions"></a><span data-ttu-id="36df5-312">Voorwaardelijke expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-312">Conditional Expressions</span></span>

<span data-ttu-id="36df5-313">Als er twee andere expressies van hetzelfde type en een booleaanse expressie zijn opgegeven, kan de voorwaardelijke expressie worden gevormd met behulp van het vraag teken `?` en de verticale balk `|` .</span><span class="sxs-lookup"><span data-stu-id="36df5-313">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="36df5-314">Bijvoorbeeld `a==b ? c | d`.</span><span class="sxs-lookup"><span data-stu-id="36df5-314">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="36df5-315">In dit voor beeld is de waarde van de voorwaardelijke expressie `c` als `a==b` True en `d` als deze False is.</span><span class="sxs-lookup"><span data-stu-id="36df5-315">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="36df5-316">Voorwaardelijke expressies met callables</span><span class="sxs-lookup"><span data-stu-id="36df5-316">Conditional expressions with callables</span></span>

<span data-ttu-id="36df5-317">De twee expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="36df5-317">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="36df5-318">In dit geval is het type van de voorwaardelijke expressie een bewerking met de invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="36df5-318">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="36df5-319">Bijvoorbeeld als `Op1` , `Op2` , en `Op3` alle zijn `Qubit[]=>Unit` , maar `Op1` ondersteunt `Adjoint` , `Op2` ondersteunt `Controlled` en `Op3` ondersteunt:</span><span class="sxs-lookup"><span data-stu-id="36df5-319">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="36df5-320">`flag ? Op1 | Op2`is een `(Qubit[] => Unit)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="36df5-320">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="36df5-321">`flag ? Op1 | Op3`is een `(Qubit[] => Unit is Adj)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="36df5-321">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="36df5-322">`flag ? Op2 | Op3`is een `(Qubit[] => Unit is Ctl)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="36df5-322">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="36df5-323">Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in het resultaat dat de waarde van de aanroep zal zijn.</span><span class="sxs-lookup"><span data-stu-id="36df5-323">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="36df5-324">Als bijvoorbeeld is ingesteld op `a==b ? C(qs) | D(qs)` True, wordt `a==b` de `C` bewerking opgeroepen en als deze ONWAAR is, `D` wordt alleen aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="36df5-324">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="36df5-325">Dit is vergelijkbaar met kort circuits in andere talen.</span><span class="sxs-lookup"><span data-stu-id="36df5-325">This is similar to short-circuiting in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="36df5-326">Aanroep bare expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-326">Callable Expressions</span></span>

<span data-ttu-id="36df5-327">Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.</span><span class="sxs-lookup"><span data-stu-id="36df5-327">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="36df5-328">Bijvoorbeeld: `X` is een letterlijke bewerkings bewerking die verwijst naar de standaard `X` -bibliotheek bewerking en `Message` is een functie-literal die verwijst naar de functie standaard bibliotheek `Message` .</span><span class="sxs-lookup"><span data-stu-id="36df5-328">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="36df5-329">Als een bewerking de `Adjoint` functor ondersteunt, `Adjoint op` is een bewerkings expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-329">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="36df5-330">Op dezelfde manier geldt dat als de bewerking de `Controlled` functor ondersteunt, `Controlled op` een bewerkings expressie is.</span><span class="sxs-lookup"><span data-stu-id="36df5-330">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="36df5-331">De typen van deze expressies worden opgegeven bij het [aanroepen van bewerkings-specials](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span><span class="sxs-lookup"><span data-stu-id="36df5-331">The types of these expressions are specified at [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="36df5-332">Functors ( `Adjoint` en `Controlled` ) binden meer nauw keuriger dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met [].</span><span class="sxs-lookup"><span data-stu-id="36df5-332">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with []\`.</span></span>
<span data-ttu-id="36df5-333">Daarom is het volgende juridisch, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="36df5-333">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="36df5-334">Met type para meter aanroep bare expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-334">Type-parameterized callable expressions</span></span>

<span data-ttu-id="36df5-335">Een aanroep bare letterlijke tekenloze kan worden gebruikt als een waarde, moet worden toegewezen aan een variabele of door gegeven aan een andere aanroepable.</span><span class="sxs-lookup"><span data-stu-id="36df5-335">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="36df5-336">Als de aanroepable van het [type para meters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)is, moeten deze als onderdeel van de aanroep bare waarde worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="36df5-336">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), they must be provided as part of the callable value.</span></span>
<span data-ttu-id="36df5-337">Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben.</span><span class="sxs-lookup"><span data-stu-id="36df5-337">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="36df5-338">Als bijvoorbeeld `Fun` een functie met hand tekening is `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="36df5-338">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="36df5-339">Aanroep bare aanroepende expressies</span><span class="sxs-lookup"><span data-stu-id="36df5-339">Callable Invocation Expressions</span></span>

<span data-ttu-id="36df5-340">Gezien een aanroep bare (Operation-of Function-) expressie en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kan een aanroep expressie worden gevormd door de tuple-expressie toe te voegen aan de aanroep bare expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-340">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="36df5-341">Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.</span><span class="sxs-lookup"><span data-stu-id="36df5-341">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="36df5-342">Als bijvoorbeeld `Op` een bewerking met hand tekening is `((Int, Qubit) => Double)` , `Op(3, qubit1)` is een expressie van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="36df5-342">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="36df5-343">Op dezelfde manier `Sin` is, als een functie met hand tekening `(Double -> Double)` , `Sin(0.1)` een expressie van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="36df5-343">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="36df5-344">Ten slotte, als `Builder` een functie met hand tekening `(Int -> (Int -> Int))` , `Builder(3)` is een functie van naar int.</span><span class="sxs-lookup"><span data-stu-id="36df5-344">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="36df5-345">Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.</span><span class="sxs-lookup"><span data-stu-id="36df5-345">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="36df5-346">Om het resultaat van aanroepen `Builder` vanuit de vorige alinea te kunnen aanroepen, is de juiste syntaxis:</span><span class="sxs-lookup"><span data-stu-id="36df5-346">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="36df5-347">Bij het aanroepen van een aanroep [bare type para meter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) kunnen de werkelijke type parameters worden opgegeven tussen punt haken `<` en `>` na de aanroep bare expressie.</span><span class="sxs-lookup"><span data-stu-id="36df5-347">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="36df5-348">Dit is doorgaans onnodig omdat de compiler Q # de daad werkelijke typen afleidt.</span><span class="sxs-lookup"><span data-stu-id="36df5-348">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="36df5-349">Het *is* echter wel vereist voor een [gedeeltelijke toepassing](xref:microsoft.quantum.guide.operationsfunctions#partial-application) als een argument van het type para meter left niet is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="36df5-349">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="36df5-350">Het is ook soms handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.</span><span class="sxs-lookup"><span data-stu-id="36df5-350">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="36df5-351">Bijvoorbeeld als `Func` hand tekening is ondertekend `('T1, 'T2, 'T1) -> 'T2` , `Op1` hand tekening heeft `Op2` `(Qubit[] => Unit is Adj)` en `Op3` hand tekening heeft, om als het `(Qubit[] => Unit)` `Func` `Op1` eerste argument `Op2` als tweede en `Op3` als derde te worden aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="36df5-351">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="36df5-352">De type specificatie is vereist omdat `Op3` en `Op1` andere typen hebben, waardoor de compiler dit als dubbel zinnig wordt behandeld zonder de specificatie.</span><span class="sxs-lookup"><span data-stu-id="36df5-352">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="36df5-353">Operator prioriteit</span><span class="sxs-lookup"><span data-stu-id="36df5-353">Operator Precedence</span></span>

<span data-ttu-id="36df5-354">Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^` .</span><span class="sxs-lookup"><span data-stu-id="36df5-354">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="36df5-355">U kunt `[` `]` voor elke operator een binding maken, en voor het segmenteren en indexeren van matrices.</span><span class="sxs-lookup"><span data-stu-id="36df5-355">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="36df5-356">De functors `Adjoint` en `Controlled` binding na het indexeren van de matrix, maar vóór alle andere opera tors.</span><span class="sxs-lookup"><span data-stu-id="36df5-356">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="36df5-357">Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.</span><span class="sxs-lookup"><span data-stu-id="36df5-357">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="36df5-358">Opera tors in volg orde van prioriteit, van hoog naar laag:</span><span class="sxs-lookup"><span data-stu-id="36df5-358">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="36df5-359">Operator</span><span class="sxs-lookup"><span data-stu-id="36df5-359">Operator</span></span> | <span data-ttu-id="36df5-360">Ariteit</span><span class="sxs-lookup"><span data-stu-id="36df5-360">Arity</span></span> | <span data-ttu-id="36df5-361">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="36df5-361">Description</span></span> | <span data-ttu-id="36df5-362">Typen operand</span><span class="sxs-lookup"><span data-stu-id="36df5-362">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="36df5-363">Volg`!`</span><span class="sxs-lookup"><span data-stu-id="36df5-363">trailing `!`</span></span> | <span data-ttu-id="36df5-364">Unaire</span><span class="sxs-lookup"><span data-stu-id="36df5-364">Unary</span></span> | <span data-ttu-id="36df5-365">Uitpakken</span><span class="sxs-lookup"><span data-stu-id="36df5-365">Unwrap</span></span> | <span data-ttu-id="36df5-366">Een door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="36df5-366">Any user-defined type</span></span>
 <span data-ttu-id="36df5-367">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="36df5-367">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="36df5-368">Unaire</span><span class="sxs-lookup"><span data-stu-id="36df5-368">Unary</span></span> | <span data-ttu-id="36df5-369">Numerieke, negatieve, bitsgewijze complement, logische negatie</span><span class="sxs-lookup"><span data-stu-id="36df5-369">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="36df5-370">`Int`, `BigInt` of voor, `Double` of voor `-` `Int` `BigInt` `~~~` , `Bool` voor`not`</span><span class="sxs-lookup"><span data-stu-id="36df5-370">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="36df5-371">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-371">Binary</span></span> | <span data-ttu-id="36df5-372">Geheel getal energie</span><span class="sxs-lookup"><span data-stu-id="36df5-372">Integer power</span></span> | <span data-ttu-id="36df5-373">`Int`of `BigInt` voor de basis `Int` voor de exponent</span><span class="sxs-lookup"><span data-stu-id="36df5-373">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="36df5-374">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="36df5-374">`/`, `*`, `%`</span></span> | <span data-ttu-id="36df5-375">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-375">Binary</span></span> | <span data-ttu-id="36df5-376">Deling, vermenigvuldiging, integer modulus</span><span class="sxs-lookup"><span data-stu-id="36df5-376">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="36df5-377">`Int`, `BigInt` of `Double` voor `/` en `*` , `Int` of `BigInt` voor`%`</span><span class="sxs-lookup"><span data-stu-id="36df5-377">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="36df5-378">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="36df5-378">`+`, `-`</span></span> | <span data-ttu-id="36df5-379">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-379">Binary</span></span> | <span data-ttu-id="36df5-380">Toevoeging of teken reeks-en matrix samenvoeging, aftrekken</span><span class="sxs-lookup"><span data-stu-id="36df5-380">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="36df5-381">`Int`, `BigInt` of `Double` , ook `String` of een matrix type voor`+`</span><span class="sxs-lookup"><span data-stu-id="36df5-381">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="36df5-382">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="36df5-382">`<<<`, `>>>`</span></span> | <span data-ttu-id="36df5-383">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-383">Binary</span></span> | <span data-ttu-id="36df5-384">Shift-links, Shift-rechts</span><span class="sxs-lookup"><span data-stu-id="36df5-384">Left shift, right shift</span></span> | <span data-ttu-id="36df5-385">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="36df5-385">`Int` or `BigInt`</span></span>
 <span data-ttu-id="36df5-386">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="36df5-386">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="36df5-387">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-387">Binary</span></span> | <span data-ttu-id="36df5-388">Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="36df5-388">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="36df5-389">`Int`, `BigInt` of`Double`</span><span class="sxs-lookup"><span data-stu-id="36df5-389">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="36df5-390">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="36df5-390">`==`, `!=`</span></span> | <span data-ttu-id="36df5-391">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-391">Binary</span></span> | <span data-ttu-id="36df5-392">gelijk, niet-gelijk-vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="36df5-392">equal, not-equal comparisons</span></span> | <span data-ttu-id="36df5-393">een primitief type</span><span class="sxs-lookup"><span data-stu-id="36df5-393">any primitive type</span></span>
 `&&&` | <span data-ttu-id="36df5-394">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-394">Binary</span></span> | <span data-ttu-id="36df5-395">Bitsgewijze AND</span><span class="sxs-lookup"><span data-stu-id="36df5-395">Bitwise AND</span></span> | <span data-ttu-id="36df5-396">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="36df5-396">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="36df5-397">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-397">Binary</span></span> | <span data-ttu-id="36df5-398">Bitsgewijze XOR</span><span class="sxs-lookup"><span data-stu-id="36df5-398">Bitwise XOR</span></span> | <span data-ttu-id="36df5-399">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="36df5-399">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="36df5-400">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-400">Binary</span></span> | <span data-ttu-id="36df5-401">Bitsgewijze OR</span><span class="sxs-lookup"><span data-stu-id="36df5-401">Bitwise OR</span></span> | <span data-ttu-id="36df5-402">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="36df5-402">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="36df5-403">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-403">Binary</span></span> | <span data-ttu-id="36df5-404">Logische en</span><span class="sxs-lookup"><span data-stu-id="36df5-404">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="36df5-405">Binair</span><span class="sxs-lookup"><span data-stu-id="36df5-405">Binary</span></span> | <span data-ttu-id="36df5-406">Logische of</span><span class="sxs-lookup"><span data-stu-id="36df5-406">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="36df5-407">Binair/Ternair</span><span class="sxs-lookup"><span data-stu-id="36df5-407">Binary/Ternary</span></span> | <span data-ttu-id="36df5-408">De operator Range</span><span class="sxs-lookup"><span data-stu-id="36df5-408">Range operator</span></span> | `Int`
 <span data-ttu-id="36df5-409">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="36df5-409">`?` `|`</span></span> | <span data-ttu-id="36df5-410">Ternair</span><span class="sxs-lookup"><span data-stu-id="36df5-410">Ternary</span></span> | <span data-ttu-id="36df5-411">Voorwaardelijk</span><span class="sxs-lookup"><span data-stu-id="36df5-411">Conditional</span></span> | <span data-ttu-id="36df5-412">`Bool`voor de linkerkant</span><span class="sxs-lookup"><span data-stu-id="36df5-412">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="36df5-413">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="36df5-413">`w/` `<-`</span></span> | <span data-ttu-id="36df5-414">Ternair</span><span class="sxs-lookup"><span data-stu-id="36df5-414">Ternary</span></span> | <span data-ttu-id="36df5-415">Kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="36df5-415">Copy-and-update</span></span> | <span data-ttu-id="36df5-416">Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="36df5-416">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="whats-next"></a><span data-ttu-id="36df5-417">Hoe nu verder?</span><span class="sxs-lookup"><span data-stu-id="36df5-417">What's Next?</span></span>
<span data-ttu-id="36df5-418">Nu u met de expressies in Q # kunt werken, kunt u de [bewerkingen en functies in q #](xref:microsoft.quantum.guide.operationsfunctions) gebruiken om te leren hoe u bewerkingen en functies definieert en aanroept.</span><span class="sxs-lookup"><span data-stu-id="36df5-418">Now that you can work with expressions in Q#, you can head to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
