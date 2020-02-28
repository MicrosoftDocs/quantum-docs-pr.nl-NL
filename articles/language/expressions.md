---
title: 'Q #-expressies'
description: 'Meer informatie over het opgeven, verwijzen en combi neren van constanten, variabelen, Opera Tors, bewerkingen en functies als expressies in Q #.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: fbde873f220d737db17f889d00be33541e3eb59b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907406"
---
# <a name="expressions"></a><span data-ttu-id="0a6e3-103">Expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-103">Expressions</span></span>

## <a name="grouping"></a><span data-ttu-id="0a6e3-104">Shapes</span><span class="sxs-lookup"><span data-stu-id="0a6e3-104">Grouping</span></span>

<span data-ttu-id="0a6e3-105">Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-105">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="0a6e3-106">`(7)` is bijvoorbeeld een `Int` expressie, `([1,2,3])` een expressie van het type matrix van `Int`s en `((1,2))` is een expressie van het type `(Int, Int)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-106">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="0a6e3-107">De equivalentie tussen eenvoudige waarden en enkele Tuples die in [het type model](xref:microsoft.quantum.language.type-model#tuple-types) worden beschreven, verwijdert de dubbel zinnigheid tussen `(6)` als een groep en `(6)` als een tuple met één element.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-107">The equivalence between simple values and single-element tuples described in [the type model](xref:microsoft.quantum.language.type-model#tuple-types) removes the ambiguity between `(6)` as a group and `(6)` as a single-element tuple.</span></span>

## <a name="symbols"></a><span data-ttu-id="0a6e3-108">Symbolen</span><span class="sxs-lookup"><span data-stu-id="0a6e3-108">Symbols</span></span>

<span data-ttu-id="0a6e3-109">De naam van een symbool dat is gekoppeld aan of is toegewezen aan een waarde van het type `'T` is een expressie van het type `'T`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-109">The name of a symbol bound or assigned to a value of type `'T` is an expression of type `'T`.</span></span>
<span data-ttu-id="0a6e3-110">Als het symbool `count` bijvoorbeeld is gebonden aan de gehele waarde `5`, is `count` een expressie voor gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-110">For instance, if the symbol `count` is bound to the integer value `5`, then `count` is an integer expression.</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="0a6e3-111">Numerieke expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-111">Numeric Expressions</span></span>

<span data-ttu-id="0a6e3-112">Numerieke expressies zijn expressies van het type `Int`, `BigInt`of `Double`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-112">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="0a6e3-113">Dat wil zeggen dat ze ofwel integeren of drijvende-komma getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-113">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="0a6e3-114">`Int` letterlijke waarden in Q # zijn identiek aan letterlijke waarden C#in het geheel getal in, behalve dat er geen ' l ' of ' l ' vereist is (of toegestaan).</span><span class="sxs-lookup"><span data-stu-id="0a6e3-114">`Int` literals in Q# are identical to integer literals in C#, except that no trailing "l" or "L" is required (or allowed).</span></span>
<span data-ttu-id="0a6e3-115">Hexadecimale en binaire gehele getallen worden respectievelijk met het voor voegsel ' 0x ' en ' 0b ' ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-115">Hexadecimal and binary integers are supported with a "0x" and "0b" prefix respectively.</span></span>

<span data-ttu-id="0a6e3-116">`BigInt` letterlijke waarden in Q # zijn gelijk aan teken reeksen met een groot geheel getal in .NET, met een afsluitende "l" of "L".</span><span class="sxs-lookup"><span data-stu-id="0a6e3-116">`BigInt` literals in Q# are identical to big integer strings in .NET, with a trailing "l" or "L".</span></span>
<span data-ttu-id="0a6e3-117">Hexadecimale Big-gehele getallen worden ondersteund met het voor voegsel 0x.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-117">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="0a6e3-118">Daarom zijn de volgende geldige toepassingen van `BigInt` literals:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-118">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="0a6e3-119">`Double` letterlijke waarden in Q # zijn identiek aan dubbele letterlijke C#waarden in, behalve dat er geen ' d ' of ' d ' vereist is (of toegestaan).</span><span class="sxs-lookup"><span data-stu-id="0a6e3-119">`Double` literals in Q# are identical to double literals in C#, except that no trailing "d" or "D" is required (or allowed).</span></span>

<span data-ttu-id="0a6e3-120">Gezien een matrix expressie van elk element type, kan een `Int`-expressie worden gevormd met behulp van de ingebouwde functie `Length`, waarbij de matrix expressie tussen haakjes, `(` en `)`is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-120">Given an array expression of any element type, an `Int` expression may be formed using the `Length` built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="0a6e3-121">Als `a` bijvoorbeeld is gebonden aan een matrix, wordt `Length(a)` een expressie voor gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-121">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="0a6e3-122">Als `b` een matrix is met gehele getallen, `Int[][]`en vervolgens `Length(b)` het aantal submatrixen in `b`en `Length(b[1])` het aantal gehele getallen in de tweede submatrix in `b`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-122">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="0a6e3-123">Als u twee numerieke expressies van hetzelfde type hebt opgegeven, kunnen de binaire Opera tors `+`, `-`, `*`en `/` worden gebruikt om een nieuwe numerieke expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-123">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="0a6e3-124">Het type van de nieuwe expressie is hetzelfde als de typen van de onderdeel expressies.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-124">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="0a6e3-125">Als u twee geheeltallige expressies hebt opgegeven, kan de binaire operator `^` (Power) worden gebruikt om een nieuwe expressie met gehele getallen te vormen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-125">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="0a6e3-126">Op dezelfde manier kan `^` worden gebruikt met twee dubbele expressies om een nieuwe dubbele expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-126">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="0a6e3-127">Ten slotte kan `^` worden gebruikt met een groot geheel getal aan de linkerkant en een geheel getal aan de rechter kant om een nieuwe Big Integer-expressie te vormen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-127">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="0a6e3-128">In dit geval moet de tweede para meter in 32 bits passen; Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-128">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="0a6e3-129">Als er twee integere of Big Integer-expressies zijn opgegeven, kan een nieuwe integer of Big Integer-expressie worden gevormd met behulp van de `%` (modulus), `&&&` (bitsgewijze AND), `|||` (bitsgewijze OR) of `^^^` (Bitsgewijze XOR)-opera tors.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-129">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="0a6e3-130">Als er een geheel getal of een Big Integer-expressie aan de linkerkant wordt gegeven en een expressie met gehele getallen aan de rechter kant, kunnen de `<<<` (reken kundige Shift-toets links) of `>>>` (reken kundige rechter verschuiving) worden gebruikt voor het maken van een nieuwe expressie met hetzelfde type als de linker expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-130">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="0a6e3-131">De tweede para meter (de waarde van de ploeg) naar een Shift-bewerking moet groter dan of gelijk aan nul zijn. het gedrag voor negatieve verschuivings bedragen is niet gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-131">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="0a6e3-132">Het aantal ploegen voor een Shift-bewerking moet ook in 32 bits passen. Als dat niet het geval is, wordt er een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-132">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="0a6e3-133">Als het getal dat moet worden verplaatst een geheel getal is, wordt het verwerkings bedrag geïnterpreteerd `mod 64`; dat wil zeggen dat een verschuiving van 1 en een verschuiving van 65 hetzelfde effect hebben.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-133">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="0a6e3-134">Voor zowel een geheel getal als een Big Integer-waarde zijn shifts reken kundig.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-134">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="0a6e3-135">Als u een negatieve waarde naar links of rechts verschuift, resulteert dit in een negatief getal.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-135">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="0a6e3-136">Dat wil zeggen dat de ene stap naar links of rechts verschuift precies hetzelfde is als vermenigvuldigen of delen met 2.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-136">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="0a6e3-137">Geheel getal en een absolute modulus volgen hetzelfde gedrag voor negatieve getallen als C#.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-137">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="0a6e3-138">Dat wil zeggen dat `a % b` altijd hetzelfde teken als `a`heeft en `b * (a / b) + a % b` altijd gelijk is aan `a`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-138">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="0a6e3-139">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-139">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="0a6e3-140">5</span><span class="sxs-lookup"><span data-stu-id="0a6e3-140">5</span></span> | <span data-ttu-id="0a6e3-141">2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-141">2</span></span> | <span data-ttu-id="0a6e3-142">2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-142">2</span></span> | <span data-ttu-id="0a6e3-143">1</span><span class="sxs-lookup"><span data-stu-id="0a6e3-143">1</span></span>
 <span data-ttu-id="0a6e3-144">5</span><span class="sxs-lookup"><span data-stu-id="0a6e3-144">5</span></span> | <span data-ttu-id="0a6e3-145">-2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-145">-2</span></span> | <span data-ttu-id="0a6e3-146">-2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-146">-2</span></span> | <span data-ttu-id="0a6e3-147">1</span><span class="sxs-lookup"><span data-stu-id="0a6e3-147">1</span></span>
 <span data-ttu-id="0a6e3-148">-5</span><span class="sxs-lookup"><span data-stu-id="0a6e3-148">-5</span></span> | <span data-ttu-id="0a6e3-149">2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-149">2</span></span> | <span data-ttu-id="0a6e3-150">-2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-150">-2</span></span> | <span data-ttu-id="0a6e3-151">-1</span><span class="sxs-lookup"><span data-stu-id="0a6e3-151">-1</span></span>
 <span data-ttu-id="0a6e3-152">-5</span><span class="sxs-lookup"><span data-stu-id="0a6e3-152">-5</span></span> | <span data-ttu-id="0a6e3-153">-2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-153">-2</span></span> | <span data-ttu-id="0a6e3-154">2</span><span class="sxs-lookup"><span data-stu-id="0a6e3-154">2</span></span> | <span data-ttu-id="0a6e3-155">-1</span><span class="sxs-lookup"><span data-stu-id="0a6e3-155">-1</span></span>

<span data-ttu-id="0a6e3-156">Het delen van een groot geheel getal en modulus werkt op dezelfde manier.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-156">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="0a6e3-157">Op basis van een numerieke expressie kan een nieuwe expressie worden gevormd met behulp van de `-` unaire operator.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-157">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="0a6e3-158">De nieuwe expressie is van hetzelfde type als de component-expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-158">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="0a6e3-159">Als een geheel getal of een Big Integer-expressie is opgegeven, kan een nieuwe expressie van hetzelfde type worden gevormd met behulp van de `~~~` (bitsgewijze complement) monadische operator.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-159">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="0a6e3-160">Booleaanse expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-160">Boolean Expressions</span></span>

<span data-ttu-id="0a6e3-161">De twee `Bool` letterlijke waarden zijn `true` en `false`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-161">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="0a6e3-162">Als u twee expressies van hetzelfde primitieve type hebt opgegeven, kunnen de binaire Opera tors `==` en `!=` worden gebruikt om een `Bool` expressie te maken.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-162">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="0a6e3-163">De expressie is waar als de twee expressies gelijk zijn en ONWAAR als dat niet het geval is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-163">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="0a6e3-164">Waarden van door de gebruiker gedefinieerde typen mogen niet worden vergeleken; alleen de waarden die worden teruggestuurd, kunnen worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-164">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="0a6e3-165">Als u bijvoorbeeld de operator ' teruglopend ' gebruikt `!` (Zie de [pagina Q # type model](xref:microsoft.quantum.language.type-model#user-defined-types)),</span><span class="sxs-lookup"><span data-stu-id="0a6e3-165">For example, using the "unwrap" operator `!` (explained in the [Q# type model page](xref:microsoft.quantum.language.type-model#user-defined-types)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="0a6e3-166">Gelijkheids vergelijking voor `Qubit` waarden is identiteits gelijkheid; dat wil zeggen of de twee expressies dezelfde Qubit identificeren.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-166">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="0a6e3-167">De status van de twee qubits wordt niet vergeleken, geopend, gemeten of gewijzigd door deze vergelijking.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-167">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="0a6e3-168">Gelijkheids vergelijking voor `Double` waarden kan misleiden door Afrondings effecten.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-168">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="0a6e3-169">Bijvoorbeeld `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-169">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="0a6e3-170">Met een wille keurige combi natie van twee numerieke expressies kunnen de binaire Opera tors `>`, `<`, `>=`en `<=` worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de eerste expressie respectievelijk groter is dan, kleiner dan, groter dan of gelijk aan, of kleiner dan of gelijk aan de tweede expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-170">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="0a6e3-171">Op basis van twee Booleaanse expressies kunnen de binaire Opera tors `and` en `or` worden gebruikt voor het maken van een nieuwe Boole-expressie die waar is als beide expressies beide zijn ingesteld op True.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-171">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="0a6e3-172">Met een booleaanse expressie kan de `not` unaire operator worden gebruikt voor het maken van een nieuwe booleaanse expressie die waar is als de component expressie False is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-172">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="0a6e3-173">Teken reeks expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-173">String Expressions</span></span>

<span data-ttu-id="0a6e3-174">Q # Hiermee kunnen teken reeksen worden gebruikt in de `fail`-instructie en de `Log`-standaard functie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-174">Q# allows strings to be used in the `fail` statement and the `Log` standard function.</span></span>

<span data-ttu-id="0a6e3-175">Teken reeksen in Q # zijn letterlijke waarden of geïnterpoleerde teken reeksen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-175">Strings in Q# are either literals or interpolated strings.</span></span>
<span data-ttu-id="0a6e3-176">Letterlijke teken reeksen zijn vergelijkbaar met letterlijke teken reeksen in de meeste talen: een reeks Unicode-tekens tussen dubbele aanhalings `"`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-176">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="0a6e3-177">In een teken reeks kan de back slash `\` worden gebruikt om een dubbel aanhalings teken te escapen en om een nieuwe regel in te voegen als `\n`, een regel terugloop als `\r`en een tab als `\t`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-177">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="0a6e3-178">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-178">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```

<span data-ttu-id="0a6e3-179">De syntaxis van Q # voor teken reeks-interpolatie is een subset C# van de 7,0-syntaxis. Q # biedt geen ondersteuning voor Verbatim-geïnterpoleerde teken reeksen (meerdere regels).</span><span class="sxs-lookup"><span data-stu-id="0a6e3-179">The Q# syntax for string interpolations is a subset of the C# 7.0 syntax; Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="0a6e3-180">Zie [*geïnterpoleerde teken reeksen*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) voor C# de syntaxis.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-180">See [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) for the C# syntax.</span></span>

<span data-ttu-id="0a6e3-181">Expressies binnen een geïnterpoleerde teken reeks volgen Q # syntaxis, geen C# syntaxis.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-181">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>
<span data-ttu-id="0a6e3-182">Een geldige Q #-expressie kan worden weer gegeven in een geïnterpoleerde teken reeks.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-182">Any valid Q# expression may appear in an interpolated string.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="0a6e3-183">Qubit-expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-183">Qubit Expressions</span></span>

<span data-ttu-id="0a6e3-184">De enige `Qubit`-expressies zijn symbolen die zijn gekoppeld aan `Qubit` waarden of matrix elementen van `Qubit` matrices.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-184">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="0a6e3-185">Er zijn geen `Qubit` letterlijke waarden.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-185">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="0a6e3-186">Pauli-expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-186">Pauli Expressions</span></span>

<span data-ttu-id="0a6e3-187">De vier `Pauli` waarden, `PauliI`, `PauliX`, `PauliY`en `PauliZ`, zijn alle geldige `Pauli` expressies.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-187">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="0a6e3-188">Behalve dat zijn de enige `Pauli`-expressies symbolen die zijn gekoppeld aan `Pauli` waarden of matrix elementen van `Pauli` matrices.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-188">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="0a6e3-189">Resultaat expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-189">Result Expressions</span></span>

<span data-ttu-id="0a6e3-190">De twee `Result` waarden, `One` en `Zero`, zijn geldige `Result` expressies.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-190">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="0a6e3-191">Behalve dat zijn de enige `Result`-expressies symbolen die zijn gekoppeld aan `Result` waarden of matrix elementen van `Result` matrices.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-191">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="0a6e3-192">Houd er met name rekening mee dat `One` niet hetzelfde is als de gehele `1`en dat er geen rechtstreekse conversie tussen deze waarden is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-192">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="0a6e3-193">Dit geldt ook voor `Zero` en `0`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-193">The same is true for `Zero` and `0`.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="0a6e3-194">Bereik expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-194">Range Expressions</span></span>

<span data-ttu-id="0a6e3-195">Als er drie `Int` expressies `start`, `step`en `stop`, is `start .. step .. stop` een bereik expressie waarvan het eerste element is `start`, het tweede element is `start+step`, het derde element is `start+step+step`, enzovoort, totdat `stop` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-195">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="0a6e3-196">Een bereik kan leeg zijn als `step` bijvoorbeeld positief is en `stop < start`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-196">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="0a6e3-197">Het laatste element van het bereik wordt `stop` als het verschil tussen `start` en `stop` een integraal veelvoud van `step`is; dat wil zeggen dat het bereik op beide uiteinden is inbegrepen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-197">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="0a6e3-198">Op basis van twee `Int` expressies `start` en `stop`is `start .. stop` een bereik expressie die gelijk is aan `start .. 1 .. stop`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-198">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="0a6e3-199">Houd er rekening mee dat de geïmpliceerde `step` + 1, zelfs als `stop` kleiner is dan `start`. in dat geval is het bereik leeg.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-199">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="0a6e3-200">Enkele voor beelden van bereiken:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-200">Some example ranges are:</span></span>

- <span data-ttu-id="0a6e3-201">`1..3` is het bereik van 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-201">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="0a6e3-202">`2..2..5` is het bereik van 2, 4.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-202">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="0a6e3-203">`2..2..6` is het bereik 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-203">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="0a6e3-204">`6..-2..2` is het bereik van 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-204">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="0a6e3-205">`2..1` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-205">`2..1` is the empty range.</span></span>
- <span data-ttu-id="0a6e3-206">`2..6..7` is het bereik 2.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-206">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="0a6e3-207">`2..2..1` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-207">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="0a6e3-208">`1..-1..2` is een leeg bereik.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-208">`1..-1..2` is the empty range.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="0a6e3-209">Aanroep bare expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-209">Callable Expressions</span></span>

<span data-ttu-id="0a6e3-210">Een aanroep bare letterlijke waarde is de naam van een bewerking of functie die is gedefinieerd in het compilatie bereik.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-210">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="0a6e3-211">`X` is bijvoorbeeld een letterlijke bewerkings bewerking die verwijst naar de standaard bibliotheek `X` bewerking en `Message` een letterlijke functie is die verwijst naar de functie standaard bibliotheek `Message`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-211">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="0a6e3-212">Als een bewerking de `Adjoint` functor ondersteunt, is `Adjoint op` een bewerkings expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-212">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="0a6e3-213">En als de bewerking de `Controlled` functor ondersteunt, is `Controlled op` een bewerkings expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-213">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="0a6e3-214">De typen van deze expressies worden opgegeven in [functors](xref:microsoft.quantum.language.type-model#functors).</span><span class="sxs-lookup"><span data-stu-id="0a6e3-214">The types of these expressions are specified in [Functors](xref:microsoft.quantum.language.type-model#functors).</span></span>

<span data-ttu-id="0a6e3-215">Functors (`Adjoint` en `Controlled`) zijn beter te binden dan alle andere opera Tors, met uitzonde ring van de operator voor uitpakken `!` en het indexeren van matrices met `[]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-215">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[]`.</span></span>
<span data-ttu-id="0a6e3-216">Daarom is het volgende juridisch, ervan uitgaande dat de bewerkingen ondersteuning bieden voor de functors die worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-216">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

<span data-ttu-id="0a6e3-217">Een aanroep bare letterlijke tekenloze kan worden gebruikt als een waarde, moet worden toegewezen aan een variabele of door gegeven aan een andere aanroepable.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-217">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="0a6e3-218">Als de aanroepable van het type para meters is, moeten deze als onderdeel van de aanroep bare waarde worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-218">In this case, if the callable has type parameters, they must be provided as part of the callable value.</span></span>
<span data-ttu-id="0a6e3-219">Een aanroep bare waarde kan geen niet-opgegeven type parameters hebben.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-219">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="0a6e3-220">Als `Fun` bijvoorbeeld een functie met hand tekening `'T1->Unit`:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-220">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="0a6e3-221">Aanroep bare aanroepende expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-221">Callable Invocation Expressions</span></span>

<span data-ttu-id="0a6e3-222">Gezien een aanroep bare (Operation-of Function-) expressie en een tuple-expressie van het invoer type van de hand tekening van de aanroepable, kan een aanroep expressie worden gevormd door de tuple-expressie toe te voegen aan de aanroep bare expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-222">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="0a6e3-223">Het type van de aanroep expressie is het uitvoer type van de hand tekening van de aanroepable.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-223">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="0a6e3-224">Als `Op` bijvoorbeeld een bewerking met een handtekening `((Int, Qubit) => Double)`is, is `Op(3, qubit1)` een expressie van het type `Double`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-224">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="0a6e3-225">Als `Sin` een functie met hand tekening `(Double -> Double)`is, is `Sin(0.1)` een expressie van het type `Double`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-225">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="0a6e3-226">Ten slotte, als `Builder` een functie met hand tekening `(Int -> (Int -> Int))`is, is `Builder(3)` een functie van tot int.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-226">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="0a6e3-227">Voor het aanroepen van het resultaat van een expressie met een aanroep bare waarde is een extra paar haakjes rond de aanroepende expressie vereist.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-227">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="0a6e3-228">Als u het resultaat van het aanroepen van `Builder` vanuit de vorige alinea wilt aanroepen, is de juiste syntaxis:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-228">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="0a6e3-229">Bij het aanroepen van een aanroep bare type para meter kunnen de werkelijke type parameters worden opgegeven tussen punt haken `<` en `>` na de aanroep bare expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-229">When invoking a type-parameterized callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="0a6e3-230">Dit is doorgaans onnodig omdat de compiler Q # de daad werkelijke typen afleidt.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-230">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="0a6e3-231">Het is vereist voor een gedeeltelijke toepassing (zie hieronder) als een argument van het type para meters niet-opgegeven is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-231">It is required for partial application (see below) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="0a6e3-232">Het is ook soms handig bij het door geven van bewerkingen met verschillende functor-ondersteuning voor een aanroepable.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-232">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="0a6e3-233">Als `Func` hand tekening heeft `('T1, 'T2, 'T1) -> 'T2`, `Op1` en `Op2` hand tekening `(Qubit[] => Unit is Adj)`heeft en `Op3` hand tekening heeft `(Qubit[] => Unit)`, om `Func` met `Op1` aan te roepen als eerste argument, `Op2` als het tweede en `Op3` als derde:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-233">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="0a6e3-234">De type specificatie is vereist omdat `Op3` en `Op1` verschillende typen hebben, zodat de compiler dit als dubbel zinnig behandelt zonder de specificatie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-234">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>

### <a name="partial-application"></a><span data-ttu-id="0a6e3-235">Gedeeltelijke toepassing</span><span class="sxs-lookup"><span data-stu-id="0a6e3-235">Partial Application</span></span>

<span data-ttu-id="0a6e3-236">Op basis van een aanroep bare expressie kan een nieuwe aanroep worden gemaakt door een subset van de argumenten op te geven die kunnen worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-236">Given a callable expression, a new callable may be created by providing a subset of the arguments to the callable.</span></span>
<span data-ttu-id="0a6e3-237">Dit wordt _gedeeltelijke toepassing_genoemd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-237">This is called _partial application_.</span></span>

<span data-ttu-id="0a6e3-238">In Q # wordt een gedeeltelijk toegepaste aanroepable weer gegeven door een expressie met een gewone aanroep te schrijven, maar met een onderstrepings teken, `_`voor de niet-opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-238">In Q#, a partially applied callable is expressed by writing a normal invocation expression, but using an underscore, `_`, for the unspecified arguments.</span></span>
<span data-ttu-id="0a6e3-239">De resulterende aanroepable heeft hetzelfde resultaat type als het basis aanroepable en dezelfde specialisatie voor bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-239">The resulting callable has the same result type as the base callable, and the same specializations for operations.</span></span>
<span data-ttu-id="0a6e3-240">Het invoer type van de gedeeltelijke toepassing is gewoon het oorspronkelijke type met de opgegeven argumenten verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-240">The input type of the partial application is simply the original type with the specified arguments removed.</span></span>

<span data-ttu-id="0a6e3-241">Als een onveranderlijke variabele wordt door gegeven als een opgegeven argument bij het maken van een gedeeltelijke toepassing, wordt de huidige waarde van de variabele gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-241">If a mutable variable is passed as a specified argument when creating a partial application, the current value of the variable is used.</span></span>
<span data-ttu-id="0a6e3-242">Als u de waarde van de variabele achteraf wijzigt, heeft dit geen invloed op de gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-242">Changing the value of the variable afterward will not impact the partial application.</span></span>

<span data-ttu-id="0a6e3-243">Als `Op` bijvoorbeeld het type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`heeft:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-243">For example, if `Op` has type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span></span>

- <span data-ttu-id="0a6e3-244">`Op(5,(_,_))` is van het type `(((Qubit,Qubit), Double) => Unit is Adj)`en is `Op(5,_)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-244">`Op(5,(_,_))` has type `(((Qubit,Qubit), Double) => Unit is Adj)`, and so has `Op(5,_)`.</span></span>
- <span data-ttu-id="0a6e3-245">`Op(_,(_,1.0))` is van het type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-245">`Op(_,(_,1.0))` has type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span></span>
- <span data-ttu-id="0a6e3-246">`Op(_,((q1,q2),_))` is van het type `((Int,Double) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-246">`Op(_,((q1,q2),_))` has type `((Int,Double) => Unit is Adj)`.</span></span>
   <span data-ttu-id="0a6e3-247">Let op: we hebben hier Singleton-tuple-equivalentie toegepast.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-247">Note that we have applied singleton tuple equivalence here.</span></span>

<span data-ttu-id="0a6e3-248">Als het gedeeltelijk toegepaste aanroep type para meters heeft die niet kunnen worden afgeleid door de compiler, moeten deze worden opgegeven op de aanroep site.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-248">If the partially-applied callable has type parameters that cannot be inferred by the compiler, they must be provided at the invocation site.</span></span>
<span data-ttu-id="0a6e3-249">De gedeeltelijke toepassing mag geen niet-opgegeven type parameters hebben.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-249">The partial application cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="0a6e3-250">Als `Op` bijvoorbeeld het type `(('T1, Qubit, 'T1) => Unit : Adjoint)`heeft:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-250">For example, if `Op` has type `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span></span>

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a><span data-ttu-id="0a6e3-251">Recursie</span><span class="sxs-lookup"><span data-stu-id="0a6e3-251">Recursion</span></span>

<span data-ttu-id="0a6e3-252">Q # callables mogen direct of indirect recursief zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-252">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="0a6e3-253">Dat wil zeggen dat een bewerking of functie zichzelf kan aanroepen, of een andere aanroep kan aanroepen die direct of indirect de aanroep bare bewerking aanroept.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-253">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="0a6e3-254">Er zijn twee belang rijke opmerkingen over het gebruik van recursie, echter:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-254">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="0a6e3-255">Het gebruik van recursie in bewerkingen heeft waarschijnlijk een conflict met bepaalde optimalisaties.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-255">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="0a6e3-256">Dit kan een aanzienlijke invloed hebben op de uitvoerings tijd van de algoritme.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-256">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="0a6e3-257">Bij het uitvoeren van een echt Quantum apparaat kan de stack-ruimte beperkt zijn en kan een grondige recursie leiden tot een runtime-fout.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-257">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="0a6e3-258">Met name de Q #-compiler en runtime identificeren en optimaliseren de staart recursie niet.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-258">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="0a6e3-259">Tuple-expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-259">Tuple Expressions</span></span>

<span data-ttu-id="0a6e3-260">Een tuple letterlijke waarde is een reeks element expressies van het juiste type, gescheiden door komma's, tussen `(` en `)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-260">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="0a6e3-261">`(1, One)` is bijvoorbeeld een `(Int, Result)`-expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-261">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="0a6e3-262">Met uitzonde ring van letterlijke waarden, de enige tuple-expressies zijn symbolen die zijn gebonden aan tuplewaarde, matrix elementen van tuple-matrices en aanroep bare aanroepen die Tuples retour neren.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-262">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="0a6e3-263">Door de gebruiker gedefinieerde type expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-263">User-Defined Type Expressions</span></span>

<span data-ttu-id="0a6e3-264">Een letterlijke waarde van een door de gebruiker gedefinieerd type bestaat uit de type naam gevolgd door een tuple letterlijke waarde van het type basis-tuple.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-264">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="0a6e3-265">Als `IntPair` bijvoorbeeld een door de gebruiker gedefinieerd type op basis van `(Int, Int)`is, dan is `IntPair(2,3)` een geldige letterlijke waarde van dat type.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-265">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2,3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="0a6e3-266">Met uitzonde ring van letterlijke waarden zijn de enige expressies van een door de gebruiker gedefinieerd type symbolen die gebonden zijn aan de waarde van dat type, matrix elementen van matrices van dat type en aanroep bare aanroepen die dat type retour neren.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-266">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="0a6e3-267">Onverpakte expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-267">Unwrap Expressions</span></span>

<span data-ttu-id="0a6e3-268">In Q # is de operator voor uitpakken een afsluitend uitroep teken `!`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-268">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="0a6e3-269">Als `IntPair` bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `(Int, Int)`is en `s` een variabele met de waarde `IntPair(2,3)`, dan zou `s!` worden `(2,3)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-269">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2,3)`, then `s!` would be `(2,3)`.</span></span>

<span data-ttu-id="0a6e3-270">Voor door de gebruiker gedefinieerde typen die zijn gedefinieerd in termen van andere door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-270">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="0a6e3-271">de operator voor uitpakken kan worden herhaald. `s!!` geeft bijvoorbeeld de dubbele waarde onverpakt op `s`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-271">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="0a6e3-272">Als `WrappedPair` bijvoorbeeld een door de gebruiker gedefinieerd type met een onderliggend type `IntPair`en `t` een variabele met de waarde `WrappedPair(IntPair(1,2))`, dan zou `t!!` worden `(1,2)`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-272">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="0a6e3-273">De operator `!` heeft een hogere prioriteit dan alle andere opera tors dan `[]` voor het indexeren van matrices en het segmenteren.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-273">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="0a6e3-274">`!` en `[]` positioneel binden; dat wil zeggen dat `a[i]![3]` moet worden gelezen als `((a[i])!)[3]`: Neem het element van de `i`van `a`, pak het uit en haal vervolgens het derde element van de niet-ingepakte waarde op (dit moet een matrix zijn).</span><span class="sxs-lookup"><span data-stu-id="0a6e3-274">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="0a6e3-275">De prioriteit van de `!` operator heeft een invloed die mogelijk niet duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-275">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="0a6e3-276">Als een functie of bewerking een waarde retourneert die vervolgens terugkeert, moet de functie-of bewerkings aanroep tussen haakjes worden geplaatst, zodat de argument tuple wordt gekoppeld aan de aanroep in plaats van naar de uitpakken.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-276">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="0a6e3-277">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-277">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="0a6e3-278">Matrix expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-278">Array Expressions</span></span>

<span data-ttu-id="0a6e3-279">Een letterlijke matrix is een reeks van een of meer element expressies, gescheiden door komma's, tussen `[` en `]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-279">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="0a6e3-280">Alle elementen moeten compatibel zijn met hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-280">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="0a6e3-281">Als het algemene element type een bewerking of functie type is, moeten alle elementen hetzelfde invoer-en uitvoer type hebben.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-281">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="0a6e3-282">Het element type van de matrix ondersteunt alle functors die door alle elementen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-282">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="0a6e3-283">Als `Op1`, `Op2`en `Op3` allemaal `Qubit[] => Unit`zijn, maar `Op1` ondersteuning biedt voor `Adjoint`, `Op2` ondersteunt `Controlled`, en `Op3` beide ondersteunen:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-283">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="0a6e3-284">`[Op1, Op2]` is een matrix met `(Qubit[] => Unit)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-284">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="0a6e3-285">`[Op1, Op3]` is een matrix met `(Qubit[] => Unit is Adj)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-285">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="0a6e3-286">`[Op2, Op3]` is een matrix met `(Qubit[] => Unit is Ctl)` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-286">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="0a6e3-287">Lege letterlijke arrays, `[]`, zijn niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-287">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="0a6e3-288">In plaats daarvan gebruikt u `new ★[0]`, waarbij `★` als tijdelijke aanduiding voor een geschikt type is, de gewenste matrix met een lengte van nul kunt maken.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-288">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="0a6e3-289">Als er twee matrices van hetzelfde type zijn opgegeven, kan de operator binary `+` worden gebruikt voor het vormen van een nieuwe matrix die de samen voeging van de twee matrices vormt.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-289">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="0a6e3-290">`[1,2,3] + [4,5,6]` is bijvoorbeeld `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-290">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="0a6e3-291">Matrix maken</span><span class="sxs-lookup"><span data-stu-id="0a6e3-291">Array Creation</span></span>

<span data-ttu-id="0a6e3-292">Op basis van een type en een `Int`-expressie kan de operator `new` worden gebruikt voor het toewijzen van een nieuwe matrix met de opgegeven grootte.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-292">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="0a6e3-293">`new Int[i+1]` zou bijvoorbeeld een nieuwe `Int` matrix met `i+1` elementen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-293">For instance, `new Int[i+1]` would allocate a new `Int` array with `i+1` elements.</span></span>

<span data-ttu-id="0a6e3-294">De elementen van een nieuwe matrix worden geïnitialiseerd op een type-afhankelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-294">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="0a6e3-295">In de meeste gevallen is dit een bepaalde variatie van nul.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-295">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="0a6e3-296">Voor qubits en callables, die verwijzingen naar entiteiten zijn, is er geen redelijke standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-296">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="0a6e3-297">Daarom is de standaard waarde voor deze typen een ongeldige verwijzing die niet kan worden gebruikt zonder dat er een runtime-fout wordt veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-297">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="0a6e3-298">Dit is vergelijkbaar met een null-verwijzing in talen zoals C# of Java.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-298">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="0a6e3-299">Matrices met qubits of callables moeten correct worden geïnitialiseerd met niet-standaard waarden voordat de elementen veilig kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-299">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="0a6e3-300">Geschikte initialisatie routines kunt u vinden in <xref:microsoft.quantum.arrays>.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-300">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="0a6e3-301">De standaard waarden voor elk type zijn:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-301">The default values for each type are:</span></span>

<span data-ttu-id="0a6e3-302">Type</span><span class="sxs-lookup"><span data-stu-id="0a6e3-302">Type</span></span> | <span data-ttu-id="0a6e3-303">Standaard</span><span class="sxs-lookup"><span data-stu-id="0a6e3-303">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="0a6e3-304">_Ongeldige Qubit_</span><span class="sxs-lookup"><span data-stu-id="0a6e3-304">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="0a6e3-305">Het lege bereik `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-305">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="0a6e3-306">_Ongeldige aanroepable_</span><span class="sxs-lookup"><span data-stu-id="0a6e3-306">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="0a6e3-307">De tuple-typen zijn geïnitialiseerd met element-by-element.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-307">Tuple types are initialized element-by-element.</span></span>


### <a name="jagged-arrays"></a><span data-ttu-id="0a6e3-308">Gekartelde matrices</span><span class="sxs-lookup"><span data-stu-id="0a6e3-308">Jagged Arrays</span></span>

<span data-ttu-id="0a6e3-309">Een gekartelde matrix, ook wel een matrix van matrices genoemd, is een matrix waarvan de elementen matrices zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-309">A jagged array, sometimes called an "array of arrays", is an array whose elements are arrays.</span></span> <span data-ttu-id="0a6e3-310">De elementen van een gekartelde matrix kunnen van verschillende grootten zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-310">The elements of a jagged array can be of different sizes.</span></span> <span data-ttu-id="0a6e3-311">In het volgende voor beeld ziet u hoe u een gekartelde matrix die een vermenigvuldigings tabel vertegenwoordigt, declareert en initialiseert.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-311">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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


### <a name="array-slices"></a><span data-ttu-id="0a6e3-312">Matrix segmenten</span><span class="sxs-lookup"><span data-stu-id="0a6e3-312">Array Slices</span></span>

<span data-ttu-id="0a6e3-313">Op basis van een matrix expressie en een `Range` expressie kan een nieuwe expressie worden gevormd met de segment operator `[` en `]` matrix.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-313">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="0a6e3-314">De nieuwe expressie is van hetzelfde type als de matrix en bevat de matrix items die worden geïndexeerd door de elementen van de `Range`, in de volg orde die wordt gedefinieerd door de `Range`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-314">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="0a6e3-315">Als `a` bijvoorbeeld is gebonden aan een matrix van `Double`s, is `a[3..-1..0]` een `Double[]`-expressie die de eerste vier elementen van `a` bevat, maar in de omgekeerde volg orde zoals ze in `a`worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-315">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="0a6e3-316">Als de `Range` leeg is, krijgt het resulterende matrix segment de lengte nul.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-316">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="0a6e3-317">Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om te kunnen worden gesegmenteerd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-317">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="0a6e3-318">Als `a` en `b` beide matrices van `Int`s zijn, wordt een segment uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-318">For instance, if `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

<span data-ttu-id="0a6e3-319">Alle matrices in Q # zijn gebaseerd op nul.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-319">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="0a6e3-320">Dat wil zeggen dat het eerste element van een matrix `a` altijd `a[0]`is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-320">That is, the first element of an array `a` is always `a[0]`.</span></span>

<span data-ttu-id="0a6e3-321">Vanaf onze 0,8-release ondersteunen we context afhankelijke expressies voor bereik segmenting.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-321">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="0a6e3-322">Met name bereik begin-en eind waarden kunnen worden wegge laten in de context van een expressie voor bereik segmentering.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-322">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="0a6e3-323">In dat geval past de compiler de volgende regels toe om de beoogde scheidings tekens voor het bereik af te leiden.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-323">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="0a6e3-324">Als de begin waarde van het bereik bijvoorbeeld wordt wegge laten, wordt de uitgestelde begin waarde</span><span class="sxs-lookup"><span data-stu-id="0a6e3-324">For example, if the range start value is omitted, then the inferred start value</span></span> 
- <span data-ttu-id="0a6e3-325">is nul als er geen stap is opgegeven of als de opgegeven stap positief is en</span><span class="sxs-lookup"><span data-stu-id="0a6e3-325">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="0a6e3-326">is de lengte van de gesegmenteerde matrix min één als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-326">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="0a6e3-327">Als de eind waarde van het bereik wordt wegge laten, wordt de uitgestelde eind waarde</span><span class="sxs-lookup"><span data-stu-id="0a6e3-327">If the range end value is omitted, then the inferred end value</span></span> 
- <span data-ttu-id="0a6e3-328">is de lengte van de gesegmenteerde matrix min één als er geen stap is opgegeven, of als de opgegeven stap positief is en</span><span class="sxs-lookup"><span data-stu-id="0a6e3-328">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="0a6e3-329">is nul als de opgegeven stap negatief is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-329">is zero if the specified step is negative.</span></span> 

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

## <a name="array-element-expressions"></a><span data-ttu-id="0a6e3-330">Matrix element expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-330">Array Element Expressions</span></span>

<span data-ttu-id="0a6e3-331">Op basis van een matrix expressie en een `Int`-expressie kan een nieuwe expressie worden gevormd met de operator `[` en `]` matrix element.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-331">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="0a6e3-332">De nieuwe expressie is van hetzelfde type als het element type van de matrix.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-332">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="0a6e3-333">Als `a` bijvoorbeeld is gebonden aan een matrix van `Double`s, is `a[4]` een `Double`-expressie.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-333">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="0a6e3-334">Als de matrix expressie geen eenvoudige id is, moet deze tussen haakjes worden geplaatst om een element te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-334">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to select an element.</span></span>
<span data-ttu-id="0a6e3-335">Als bijvoorbeeld `a` en `b` beide matrices van `Int`s zijn, wordt een element uit de samen voeging als volgt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-335">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[13]
```

<span data-ttu-id="0a6e3-336">Alle matrices in Q # zijn gebaseerd op nul.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-336">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="0a6e3-337">Dat wil zeggen dat het eerste element van een matrix `a` altijd `a[0]`is.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-337">That is, the first element of an array `a` is always `a[0]`.</span></span>


## <a name="copy-and-update-expressions"></a><span data-ttu-id="0a6e3-338">Expressies kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a6e3-338">Copy-and-Update Expressions</span></span>

<span data-ttu-id="0a6e3-339">Nieuwe matrices kunnen worden gemaakt op basis van bestaande met behulp van Copy-en-update-expressies.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-339">New arrays can be created from existing ones via copy-and-update expressions.</span></span>
<span data-ttu-id="0a6e3-340">Een copy-en-update-expressie is een expressie van het formulier `expression1 w/ expression2 <- expression3`, waarbij `expression1` van het type `T[]` moet zijn voor bepaalde typen `T`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-340">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span> <span data-ttu-id="0a6e3-341">De tweede `expression2` definieert de indices van de element (en) die moeten worden gewijzigd vergeleken met de matrix in `expression1` en moet een type `Int` of van het type `Range`zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-341">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span> <span data-ttu-id="0a6e3-342">Als `expression2` van het type `Int`is, moet `expression3` van het type `T`zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-342">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="0a6e3-343">Als `expression2` van het type `Range`is, moet `expression3` van het type `T[]`zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-343">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="0a6e3-344">Met een copy-and-update-expressie `arr w/ idx <- value` wordt een nieuwe matrix gemaakt met alle elementen die zijn ingesteld op het overeenkomstige element in `arr`, met uitzonde ring van het element (en) op `idx`, die zijn ingesteld op een of meer in `value`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-344">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="0a6e3-345">Als `arr` bijvoorbeeld een matrix `[0,1,2,3]`bevat,</span><span class="sxs-lookup"><span data-stu-id="0a6e3-345">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="0a6e3-346">`arr w/ 0 <- 10` is de matrix `[10,1,2,3]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-346">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="0a6e3-347">`arr w/ 2 <- 10` is de matrix `[0,1,10,3]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-347">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="0a6e3-348">`arr w/ 0..2..3 <- [10,12]` is de matrix `[10,1,12,3]`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-348">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

<span data-ttu-id="0a6e3-349">Er bestaan soort gelijke expressies voor benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-349">Similar expressions exist for named items in user-defined types.</span></span> <span data-ttu-id="0a6e3-350">Denk bijvoorbeeld aan het type</span><span class="sxs-lookup"><span data-stu-id="0a6e3-350">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="0a6e3-351">Als `c` de waarde van het type `Complex(1.,-1.)`bevat, is `c w/ Re <- 0.` een expressie van het type `Complex` die als `Complex(0.,-1.)`wordt geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-351">If `c` contains the value of type `Complex(1.,-1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0.,-1.)`.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="0a6e3-352">Voorwaardelijke expressies</span><span class="sxs-lookup"><span data-stu-id="0a6e3-352">Conditional Expressions</span></span>

<span data-ttu-id="0a6e3-353">Als er twee andere expressies van hetzelfde type en een booleaanse expressie worden opgegeven, kan de voorwaardelijke expressie worden gevormd met behulp van het vraag teken `?` en de verticale balk `|`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-353">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="0a6e3-354">Bijvoorbeeld `a==b ? c | d`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-354">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="0a6e3-355">In dit voor beeld wordt de waarde van de voorwaardelijke expressie `c` als `a==b` waar is en `d` als deze is ingesteld op false.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-355">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

<span data-ttu-id="0a6e3-356">De twee expressies kunnen resulteren in bewerkingen die dezelfde invoer en uitvoer hebben, maar verschillende functors ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-356">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="0a6e3-357">In dit geval is het type van de voorwaardelijke expressie een bewerking met de invoer en uitvoer die ondersteuning bieden voor functors die door beide expressies worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-357">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="0a6e3-358">Als `Op1`, `Op2`en `Op3` allemaal `Qubit[]=>Unit`zijn, maar `Op1` ondersteuning biedt voor `Adjoint`, `Op2` ondersteunt `Controlled`, en `Op3` beide ondersteunen:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-358">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="0a6e3-359">`flag ? Op1 | Op2` is een `(Qubit[] => Unit)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-359">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="0a6e3-360">`flag ? Op1 | Op3` is een `(Qubit[] => Unit is Adj)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-360">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="0a6e3-361">`flag ? Op2 | Op3` is een `(Qubit[] => Unit is Ctl)` bewerking.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-361">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="0a6e3-362">Als een van de twee mogelijke resultaat expressies een functie of een bewerkings aanroep bevat, wordt die aanroep alleen uitgevoerd als dat resulteert in het resultaat dat de waarde van de aanroep zal zijn.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-362">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="0a6e3-363">Als `a==b` bijvoorbeeld is ingesteld `a==b ? C(qs) | D(qs)`op True, wordt de `C`-bewerking aangeroepen en als deze ONWAAR is, wordt alleen `D` aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-363">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="0a6e3-364">Dit is vergelijkbaar met kort circuits in andere talen.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-364">This is similar to short-circuiting in other languages.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="0a6e3-365">Operator prioriteit</span><span class="sxs-lookup"><span data-stu-id="0a6e3-365">Operator Precedence</span></span>

<span data-ttu-id="0a6e3-366">Alle binaire Opera tors zijn rechts gekoppeld, met uitzonde ring van `^`.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-366">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="0a6e3-367">De vier Kante haken, `[` en `]`, voor het segmenteren en indexeren van matrices, bind vóór een operator.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-367">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="0a6e3-368">De functors-`Adjoint` en `Controlled` BIND na het indexeren van de matrix, maar vóór alle andere opera tors.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-368">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="0a6e3-369">Tussen haakjes voor Operation-en functie aanroep moet u ook een operator binden, maar na het indexeren van matrices en functors.</span><span class="sxs-lookup"><span data-stu-id="0a6e3-369">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="0a6e3-370">Opera tors in volg orde van prioriteit, van hoog naar laag:</span><span class="sxs-lookup"><span data-stu-id="0a6e3-370">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="0a6e3-371">Operator</span><span class="sxs-lookup"><span data-stu-id="0a6e3-371">Operator</span></span> | <span data-ttu-id="0a6e3-372">Ariteit</span><span class="sxs-lookup"><span data-stu-id="0a6e3-372">Arity</span></span> | <span data-ttu-id="0a6e3-373">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0a6e3-373">Description</span></span> | <span data-ttu-id="0a6e3-374">Typen operand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-374">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="0a6e3-375">afsluitende `!`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-375">trailing `!`</span></span> | <span data-ttu-id="0a6e3-376">Monadische</span><span class="sxs-lookup"><span data-stu-id="0a6e3-376">Unary</span></span> | <span data-ttu-id="0a6e3-377">Uitpakken</span><span class="sxs-lookup"><span data-stu-id="0a6e3-377">Unwrap</span></span> | <span data-ttu-id="0a6e3-378">Een door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="0a6e3-378">Any user-defined type</span></span>
 <span data-ttu-id="0a6e3-379">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-379">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="0a6e3-380">Monadische</span><span class="sxs-lookup"><span data-stu-id="0a6e3-380">Unary</span></span> | <span data-ttu-id="0a6e3-381">Numerieke, negatieve, bitsgewijze complement, logische negatie</span><span class="sxs-lookup"><span data-stu-id="0a6e3-381">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="0a6e3-382">`Int`, `BigInt` of `Double` voor `-`, `Int` of `BigInt` voor `~~~`, `Bool` voor `not`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-382">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="0a6e3-383">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-383">Binary</span></span> | <span data-ttu-id="0a6e3-384">Geheel getal energie</span><span class="sxs-lookup"><span data-stu-id="0a6e3-384">Integer power</span></span> | <span data-ttu-id="0a6e3-385">`Int` of `BigInt` voor de basis, `Int` voor de exponent</span><span class="sxs-lookup"><span data-stu-id="0a6e3-385">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="0a6e3-386">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-386">`/`, `*`, `%`</span></span> | <span data-ttu-id="0a6e3-387">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-387">Binary</span></span> | <span data-ttu-id="0a6e3-388">Deling, vermenigvuldiging, integer modulus</span><span class="sxs-lookup"><span data-stu-id="0a6e3-388">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="0a6e3-389">`Int`, `BigInt` of `Double` voor `/` en `*`, `Int` of `BigInt` voor `%`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-389">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="0a6e3-390">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-390">`+`, `-`</span></span> | <span data-ttu-id="0a6e3-391">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-391">Binary</span></span> | <span data-ttu-id="0a6e3-392">Toevoeging of teken reeks-en matrix samenvoeging, aftrekken</span><span class="sxs-lookup"><span data-stu-id="0a6e3-392">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="0a6e3-393">`Int`, `BigInt` of `Double`, ook `String` of een wille keurig type matrix voor `+`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-393">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="0a6e3-394">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-394">`<<<`, `>>>`</span></span> | <span data-ttu-id="0a6e3-395">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-395">Binary</span></span> | <span data-ttu-id="0a6e3-396">Shift-links, Shift-rechts</span><span class="sxs-lookup"><span data-stu-id="0a6e3-396">Left shift, right shift</span></span> | <span data-ttu-id="0a6e3-397">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-397">`Int` or `BigInt`</span></span>
 <span data-ttu-id="0a6e3-398">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-398">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="0a6e3-399">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-399">Binary</span></span> | <span data-ttu-id="0a6e3-400">Kleiner dan, kleiner dan of gelijk aan, groter dan, groter dan-of-gelijk aan vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="0a6e3-400">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="0a6e3-401">`Int`, `BigInt` of `Double`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-401">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="0a6e3-402">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-402">`==`, `!=`</span></span> | <span data-ttu-id="0a6e3-403">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-403">Binary</span></span> | <span data-ttu-id="0a6e3-404">gelijk, niet-gelijk-vergelijkingen</span><span class="sxs-lookup"><span data-stu-id="0a6e3-404">equal, not-equal comparisons</span></span> | <span data-ttu-id="0a6e3-405">een primitief type</span><span class="sxs-lookup"><span data-stu-id="0a6e3-405">any primitive type</span></span>
 `&&&` | <span data-ttu-id="0a6e3-406">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-406">Binary</span></span> | <span data-ttu-id="0a6e3-407">Bitsgewijze AND</span><span class="sxs-lookup"><span data-stu-id="0a6e3-407">Bitwise AND</span></span> | <span data-ttu-id="0a6e3-408">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-408">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="0a6e3-409">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-409">Binary</span></span> | <span data-ttu-id="0a6e3-410">Bitsgewijze XOR</span><span class="sxs-lookup"><span data-stu-id="0a6e3-410">Bitwise XOR</span></span> | <span data-ttu-id="0a6e3-411">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-411">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="0a6e3-412">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-412">Binary</span></span> | <span data-ttu-id="0a6e3-413">Bitsgewijze OR</span><span class="sxs-lookup"><span data-stu-id="0a6e3-413">Bitwise OR</span></span> | <span data-ttu-id="0a6e3-414">`Int` of `BigInt`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-414">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="0a6e3-415">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-415">Binary</span></span> | <span data-ttu-id="0a6e3-416">Logische en</span><span class="sxs-lookup"><span data-stu-id="0a6e3-416">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="0a6e3-417">Binair bestand</span><span class="sxs-lookup"><span data-stu-id="0a6e3-417">Binary</span></span> | <span data-ttu-id="0a6e3-418">Logische of</span><span class="sxs-lookup"><span data-stu-id="0a6e3-418">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="0a6e3-419">Binair/Ternair</span><span class="sxs-lookup"><span data-stu-id="0a6e3-419">Binary/Ternary</span></span> | <span data-ttu-id="0a6e3-420">De operator Range</span><span class="sxs-lookup"><span data-stu-id="0a6e3-420">Range operator</span></span> | `Int`
 <span data-ttu-id="0a6e3-421">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-421">`?` `|`</span></span> | <span data-ttu-id="0a6e3-422">Ternair</span><span class="sxs-lookup"><span data-stu-id="0a6e3-422">Ternary</span></span> | <span data-ttu-id="0a6e3-423">Voorwaardelijk</span><span class="sxs-lookup"><span data-stu-id="0a6e3-423">Conditional</span></span> | <span data-ttu-id="0a6e3-424">`Bool` voor de linkerkant</span><span class="sxs-lookup"><span data-stu-id="0a6e3-424">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="0a6e3-425">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="0a6e3-425">`w/` `<-`</span></span> | <span data-ttu-id="0a6e3-426">Ternair</span><span class="sxs-lookup"><span data-stu-id="0a6e3-426">Ternary</span></span> | <span data-ttu-id="0a6e3-427">Kopiëren en bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a6e3-427">Copy-and-update</span></span> | <span data-ttu-id="0a6e3-428">Zie [expressies voor kopiëren en bijwerken](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="0a6e3-428">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>
