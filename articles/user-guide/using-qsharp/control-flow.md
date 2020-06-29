---
title: 'Controle stroom in Q #'
description: Lussen, voor waarden enzovoort.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 0cf62a128170bd0c28ff77f00fc23414567b1ea4
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415300"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="19d51-103">Controle stroom in Q #</span><span class="sxs-lookup"><span data-stu-id="19d51-103">Control flow in Q#</span></span>

<span data-ttu-id="19d51-104">Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met andere gebruikelijke, klassieke talen.</span><span class="sxs-lookup"><span data-stu-id="19d51-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="19d51-105">U kunt de controle stroom echter op drie verschillende manieren wijzigen:</span><span class="sxs-lookup"><span data-stu-id="19d51-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="19d51-106">`if`instructies</span><span class="sxs-lookup"><span data-stu-id="19d51-106">`if` statements</span></span>
* <span data-ttu-id="19d51-107">`for`lussen</span><span class="sxs-lookup"><span data-stu-id="19d51-107">`for` loops</span></span>
* <span data-ttu-id="19d51-108">`repeat-until-success`lussen</span><span class="sxs-lookup"><span data-stu-id="19d51-108">`repeat-until-success` loops</span></span>

<span data-ttu-id="19d51-109">De `if` `for` constructies en de controle stroom worden door gegeven in een vertrouwde zin voor de meeste klassieke programmeer talen.</span><span class="sxs-lookup"><span data-stu-id="19d51-109">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="19d51-110">[`Repeat-until-success`](#repeat-until-success-loop)lussen worden verderop in dit artikel besproken.</span><span class="sxs-lookup"><span data-stu-id="19d51-110">[`Repeat-until-success`](#repeat-until-success-loop) loops are discussed later in this article.</span></span>

<span data-ttu-id="19d51-111">Belang rijk: `for` lussen en `if` instructies kunnen worden gebruikt in bewerkingen waarvoor automatisch een [specialisatie](xref:microsoft.quantum.guide.operationsfunctions) wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-111">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="19d51-112">In dat scenario keert de adjoint van een `for` lus de richting om en neemt de adjoint van elke iteratie toe.</span><span class="sxs-lookup"><span data-stu-id="19d51-112">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="19d51-113">Met deze actie wordt het principe ' schoenen en SOCKS ' gehanteerd: als u het maken van een SOCKS-en vervolgens schoenen wilt opheffen, moet u de toevoeging op schoenen ongedaan maken en vervolgens op SOCKS ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="19d51-113">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="19d51-114">If, else-if, else</span><span class="sxs-lookup"><span data-stu-id="19d51-114">If, Else-if, Else</span></span>

<span data-ttu-id="19d51-115">De `if` instructie ondersteunt voorwaardelijke uitvoering.</span><span class="sxs-lookup"><span data-stu-id="19d51-115">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="19d51-116">Het bestaat uit het sleutel woord `if` , een Boole-expressie tussen haakjes en een instructie blok (de _vervolgens_ blok kering).</span><span class="sxs-lookup"><span data-stu-id="19d51-116">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="19d51-117">U kunt eventueel elk wille keurig aantal else-if-componenten volgen, elk met het sleutel woord `elif` , een Boole-expressie tussen haakjes en een instructie blok (het _else-if-_ blok).</span><span class="sxs-lookup"><span data-stu-id="19d51-117">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="19d51-118">Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).</span><span class="sxs-lookup"><span data-stu-id="19d51-118">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="19d51-119">De `if` voor waarde wordt geëvalueerd en als deze *waar*is, wordt *then* de blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-119">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="19d51-120">Als de voor waarde *Onwaar*is, wordt de eerste else-if-voor waarde geëvalueerd; Als dat het geval is, wordt de *else-if-* blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-120">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="19d51-121">Als dat niet het geval is, wordt het tweede else-if-blok geëvalueerd en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.</span><span class="sxs-lookup"><span data-stu-id="19d51-121">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="19d51-122">*Als de voor waarde origineel* en alle else-if-componenten resulteren in *Onwaar*, wordt het *else* -blok uitgevoerd, indien opgegeven.</span><span class="sxs-lookup"><span data-stu-id="19d51-122">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="19d51-123">Houd er rekening mee dat elk blok wordt uitgevoerd binnen een eigen bereik.</span><span class="sxs-lookup"><span data-stu-id="19d51-123">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="19d51-124">Bindingen die zijn gemaakt in een `if` , `elif` of `else` blok zijn niet zichtbaar nadat de blok kering is beëindigd.</span><span class="sxs-lookup"><span data-stu-id="19d51-124">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="19d51-125">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="19d51-125">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="19d51-126">of</span><span class="sxs-lookup"><span data-stu-id="19d51-126">or</span></span>
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a><span data-ttu-id="19d51-127">For-lus</span><span class="sxs-lookup"><span data-stu-id="19d51-127">For loop</span></span>

<span data-ttu-id="19d51-128">De `for` instructie ondersteunt herhalingen over een bereik met gehele getallen of een matrix.</span><span class="sxs-lookup"><span data-stu-id="19d51-128">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="19d51-129">De instructie bestaat uit het tref woord `for` , gevolgd door een symbool of symbool tuple, het tref woord `in` en een expressie van het type `Range` of de matrix, alle tussen haakjes en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="19d51-129">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="19d51-130">Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met het gedefinieerde symbool (de variabele lus) dat is gekoppeld aan elke waarde in het bereik of de matrix.</span><span class="sxs-lookup"><span data-stu-id="19d51-130">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="19d51-131">Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-131">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="19d51-132">De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-132">The expression is fully evaluated before entering the loop, and does not change while the loop is executing.</span></span>

<span data-ttu-id="19d51-133">De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en is aan het einde van de hoofd tekst losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="19d51-133">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="19d51-134">De lus-variabele is niet gebonden nadat de for-lus is voltooid.</span><span class="sxs-lookup"><span data-stu-id="19d51-134">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="19d51-135">De binding van de lus-variabele is onveranderbaar en volgt dezelfde regels als andere variabele bindingen.</span><span class="sxs-lookup"><span data-stu-id="19d51-135">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="19d51-136">In deze voor beelden `qubits` is een REGI ster van qubits (bijvoorbeeld type `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="19d51-136">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="19d51-137">Houd er rekening mee dat aan het einde de reken kundige-Shift-Left-operator wordt gebruikt `<<<` .</span><span class="sxs-lookup"><span data-stu-id="19d51-137">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="19d51-138">Zie [numerieke expressies](xref:microsoft.quantum.guide.expressions#numeric-expressions)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="19d51-138">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="19d51-139">Herhalen-tot-succes-lus</span><span class="sxs-lookup"><span data-stu-id="19d51-139">Repeat-until-success loop</span></span>

<span data-ttu-id="19d51-140">De Q #-taal staat de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.</span><span class="sxs-lookup"><span data-stu-id="19d51-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="19d51-141">Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="19d51-141">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="19d51-142">Voor beelden hiervan zijn de patronen *herhalen tot en met succes* (RUS) in Q #.</span><span class="sxs-lookup"><span data-stu-id="19d51-142">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="19d51-143">Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben. de gefactureerde kosten zijn afhankelijk van de daad werkelijke uitvoering en de interleaving van de meerdere mogelijke vertakkingen.</span><span class="sxs-lookup"><span data-stu-id="19d51-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="19d51-144">Q # ondersteunt de constructs om herhaalde tot geslaagde patronen (RUS) te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="19d51-144">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="19d51-145">waar `expression` is een geldige expressie die resulteert in een waarde van het type `Bool` .</span><span class="sxs-lookup"><span data-stu-id="19d51-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="19d51-146">De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="19d51-146">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="19d51-147">Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.</span><span class="sxs-lookup"><span data-stu-id="19d51-147">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="19d51-148">Alle drie delen van een RUS-lus (de hoofd tekst, de test en de reparatie) worden beschouwd als één bereik *voor elke herhaling*, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in zowel de test als de reparatie.</span><span class="sxs-lookup"><span data-stu-id="19d51-148">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="19d51-149">Het volt ooien van de uitvoering van de reparatie beëindigt echter het bereik voor de instructie, zodat symbool bindingen die zijn gemaakt in de hoofd tekst of de reparatie, niet beschikbaar zijn in volgende herhalingen.</span><span class="sxs-lookup"><span data-stu-id="19d51-149">However, completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="19d51-150">Verder is de `fixup` instructie vaak handig, maar niet altijd nodig.</span><span class="sxs-lookup"><span data-stu-id="19d51-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="19d51-151">In gevallen dat het niet nodig is, de construct</span><span class="sxs-lookup"><span data-stu-id="19d51-151">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="19d51-152">is ook een geldig RUS-patroon.</span><span class="sxs-lookup"><span data-stu-id="19d51-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="19d51-153">Zie voor meer voor beelden en Details [herhalen](#repeat-until-success-examples) in dit artikel.</span><span class="sxs-lookup"><span data-stu-id="19d51-153">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="19d51-154">Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions.</span><span class="sxs-lookup"><span data-stu-id="19d51-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="19d51-155">Gebruik *while* -lussen om de bijbehorende functionaliteit binnen functions te bieden.</span><span class="sxs-lookup"><span data-stu-id="19d51-155">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="19d51-156">Lus while</span><span class="sxs-lookup"><span data-stu-id="19d51-156">While loop</span></span>

<span data-ttu-id="19d51-157">Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation.</span><span class="sxs-lookup"><span data-stu-id="19d51-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="19d51-158">Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, dus de speciale taal construct in Q #.</span><span class="sxs-lookup"><span data-stu-id="19d51-158">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="19d51-159">Lussen die worden onderbroken op basis van een voor waarde en waarvan de uitvoerings lengte daarom onbekend is tijdens de compilatie, worden met name behandeld in een Quantum runtime.</span><span class="sxs-lookup"><span data-stu-id="19d51-159">However, loops that break based on a condition and whose execution length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="19d51-160">Hun gebruik in functions is echter ongevoelig omdat deze lussen alleen code bevatten die wordt uitgevoerd op conventionele hardware (niet-Quantum).</span><span class="sxs-lookup"><span data-stu-id="19d51-160">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="19d51-161">Q # biedt daarom ondersteuning voor het gebruik van while-lussen in functions.</span><span class="sxs-lookup"><span data-stu-id="19d51-161">Q#, therefore, supports to use of while loops within functions only.</span></span> <span data-ttu-id="19d51-162">Een `while` instructie bestaat uit het tref woord `while` , een Boole-expressie tussen haakjes en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="19d51-162">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="19d51-163">Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd `true` .</span><span class="sxs-lookup"><span data-stu-id="19d51-163">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a><span data-ttu-id="19d51-164">Instructie return</span><span class="sxs-lookup"><span data-stu-id="19d51-164">Return Statement</span></span>

<span data-ttu-id="19d51-165">De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="19d51-165">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="19d51-166">Het bestaat uit het tref woord `return` , gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="19d51-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="19d51-167">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="19d51-167">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="19d51-168">of</span><span class="sxs-lookup"><span data-stu-id="19d51-168">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="19d51-169">Een aanroepable die een lege tuple retourneert, `()` heeft geen instructie return nodig.</span><span class="sxs-lookup"><span data-stu-id="19d51-169">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="19d51-170">Als u een vroege afsluiting van de bewerking of functie wilt opgeven, gebruikt u `return ();` .</span><span class="sxs-lookup"><span data-stu-id="19d51-170">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="19d51-171">Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.</span><span class="sxs-lookup"><span data-stu-id="19d51-171">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="19d51-172">Er is geen maximum aantal retour instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="19d51-172">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="19d51-173">De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="19d51-173">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="19d51-174">Fout instructie</span><span class="sxs-lookup"><span data-stu-id="19d51-174">Fail statement</span></span>

<span data-ttu-id="19d51-175">De instructie Fail beëindigt het uitvoeren van een bewerking en retourneert een fout waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="19d51-175">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="19d51-176">Het bevat het tref woord `fail` , gevolgd door een teken reeks en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="19d51-176">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="19d51-177">De instructie retourneert de teken reeks naar het klassieke stuur programma als het fout bericht.</span><span class="sxs-lookup"><span data-stu-id="19d51-177">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="19d51-178">Er is geen beperking voor het aantal mislukte instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="19d51-178">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="19d51-179">De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="19d51-179">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="19d51-180">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="19d51-180">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="19d51-181">of, met behulp van [geïnterpoleerde teken reeksen](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="19d51-181">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="19d51-182">Herhalen-tot-geslaagde voor beelden</span><span class="sxs-lookup"><span data-stu-id="19d51-182">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="19d51-183">RUS-patroon voor Qubit draaiing over een Irrational-as</span><span class="sxs-lookup"><span data-stu-id="19d51-183">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="19d51-184">In een typische use-case implementeert de volgende Q #-bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt {5} $ op de Bloch-bol.</span><span class="sxs-lookup"><span data-stu-id="19d51-184">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="19d51-185">De implementatie maakt gebruik van een bekend RUS-patroon:</span><span class="sxs-lookup"><span data-stu-id="19d51-185">The implementation uses a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="19d51-186">RUS-lus met een onveranderlijke variabele in het bereik</span><span class="sxs-lookup"><span data-stu-id="19d51-186">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="19d51-187">In dit voor beeld ziet u het gebruik van een onveranderlijke variabele, `finished` die binnen het bereik van de volledige herhaling-until-reupdate-lus ligt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.</span><span class="sxs-lookup"><span data-stu-id="19d51-187">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a><span data-ttu-id="19d51-188">RUS zonder`fixup`</span><span class="sxs-lookup"><span data-stu-id="19d51-188">RUS without `fixup`</span></span>

<span data-ttu-id="19d51-189">In dit voor beeld ziet u een RUS-lus zonder de stap voor de reparatie.</span><span class="sxs-lookup"><span data-stu-id="19d51-189">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="19d51-190">De code is een Probabilistic-circuit dat een belang rijke rotatie poort implementeert $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ met behulp van de- `H` en- `T` poorten.</span><span class="sxs-lookup"><span data-stu-id="19d51-190">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="19d51-191">De lus eindigt op gemiddeld $ \frac {8} {5} $ herhalingen.</span><span class="sxs-lookup"><span data-stu-id="19d51-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="19d51-192">Zie [*herhalen-tot-geslaagd: niet-deterministische ontleding van single-Qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick en Svore, 2014) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="19d51-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="19d51-193">RUS om een Quantum status voor te bereiden</span><span class="sxs-lookup"><span data-stu-id="19d51-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="19d51-194">Ten slotte is hier een voor beeld van een RUS-patroon voor het voorbereiden van een Quantum status $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, te beginnen bij de status $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="19d51-194">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="19d51-195">Belang rijke programmeer functies die in deze bewerking worden weer gegeven, zijn:</span><span class="sxs-lookup"><span data-stu-id="19d51-195">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="19d51-196">Een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen betrokken zijn.</span><span class="sxs-lookup"><span data-stu-id="19d51-196">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="19d51-197">Het gebruik van `AssertProb` instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="19d51-197">The use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="19d51-198">[`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) Zie [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging)voor meer informatie over de-en-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="19d51-198">For more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="19d51-199">Voor meer informatie, zie voor [beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="19d51-199">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="19d51-200">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="19d51-200">Next steps</span></span>

<span data-ttu-id="19d51-201">Meer informatie over [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging) in Q #.</span><span class="sxs-lookup"><span data-stu-id="19d51-201">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
