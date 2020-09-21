---
title: Controle stroom in Q#
description: Lussen, voor waarden enzovoort.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: 547c57cab67443e8b487bf817eb79fc922b43cdc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833508"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="db309-103">Controle stroom in Q#</span><span class="sxs-lookup"><span data-stu-id="db309-103">Control flow in Q#</span></span>

<span data-ttu-id="db309-104">Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met andere gebruikelijke, klassieke talen.</span><span class="sxs-lookup"><span data-stu-id="db309-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="db309-105">U kunt de controle stroom echter op drie verschillende manieren wijzigen:</span><span class="sxs-lookup"><span data-stu-id="db309-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="db309-106">`if` instructies</span><span class="sxs-lookup"><span data-stu-id="db309-106">`if` statements</span></span>
* <span data-ttu-id="db309-107">`for` lussen</span><span class="sxs-lookup"><span data-stu-id="db309-107">`for` loops</span></span>
* <span data-ttu-id="db309-108">`repeat-until-success` lussen</span><span class="sxs-lookup"><span data-stu-id="db309-108">`repeat-until-success` loops</span></span>
* <span data-ttu-id="db309-109">conjugations (- `apply-within` instructies)</span><span class="sxs-lookup"><span data-stu-id="db309-109">conjugations (`apply-within` statements)</span></span>

<span data-ttu-id="db309-110">De `if` `for` constructies en de controle stroom worden door gegeven in een vertrouwde zin voor de meeste klassieke programmeer talen.</span><span class="sxs-lookup"><span data-stu-id="db309-110">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="db309-111">[`Repeat-until-success`](#repeat-until-success-loop) lussen en [conjugations](#conjugations) worden verderop in dit artikel besproken.</span><span class="sxs-lookup"><span data-stu-id="db309-111">[`Repeat-until-success`](#repeat-until-success-loop) loops and [conjugations](#conjugations) are discussed later in this article.</span></span>

<span data-ttu-id="db309-112">Belang rijk: `for` lussen en `if` instructies kunnen worden gebruikt in bewerkingen waarvoor automatisch een [specialisatie](xref:microsoft.quantum.guide.operationsfunctions) wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="db309-112">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="db309-113">In dat scenario keert de adjoint van een `for` lus de richting om en neemt de adjoint van elke iteratie toe.</span><span class="sxs-lookup"><span data-stu-id="db309-113">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="db309-114">Met deze actie wordt het principe ' schoenen en SOCKS ' gehanteerd: als u het maken van een SOCKS-en vervolgens schoenen wilt opheffen, moet u de toevoeging op schoenen ongedaan maken en vervolgens op SOCKS ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="db309-114">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="db309-115">If, else-if, else</span><span class="sxs-lookup"><span data-stu-id="db309-115">If, Else-if, Else</span></span>

<span data-ttu-id="db309-116">De `if` instructie ondersteunt voorwaardelijke verwerking.</span><span class="sxs-lookup"><span data-stu-id="db309-116">The `if` statement supports conditional processing.</span></span>
<span data-ttu-id="db309-117">Het bestaat uit het sleutel woord `if` , een Boole-expressie tussen haakjes en een instructie blok (de _vervolgens_ blok kering).</span><span class="sxs-lookup"><span data-stu-id="db309-117">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="db309-118">U kunt eventueel elk wille keurig aantal else-if-componenten volgen, elk met het sleutel woord `elif` , een Boole-expressie tussen haakjes en een instructie blok (het _else-if-_ blok).</span><span class="sxs-lookup"><span data-stu-id="db309-118">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="db309-119">Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).</span><span class="sxs-lookup"><span data-stu-id="db309-119">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="db309-120">De `if` voor waarde wordt geëvalueerd en als deze *waar*is, wordt *then* de blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="db309-120">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="db309-121">Als de voor waarde *Onwaar*is, wordt de eerste else-if-voor waarde geëvalueerd; Als dat het geval is, wordt de *else-if-* blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="db309-121">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="db309-122">Als dat niet het geval is, wordt het tweede else-if-blok geëvalueerd en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.</span><span class="sxs-lookup"><span data-stu-id="db309-122">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="db309-123">*Als de voor waarde origineel* en alle else-if-componenten resulteren in *Onwaar*, wordt het *else* -blok uitgevoerd, indien opgegeven.</span><span class="sxs-lookup"><span data-stu-id="db309-123">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="db309-124">Houd er rekening mee dat elk blok wordt uitgevoerd binnen een eigen bereik.</span><span class="sxs-lookup"><span data-stu-id="db309-124">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="db309-125">Bindingen die zijn gemaakt in een `if` , `elif` of `else` blok zijn niet zichtbaar nadat de blok kering is beëindigd.</span><span class="sxs-lookup"><span data-stu-id="db309-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="db309-126">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="db309-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="db309-127">of</span><span class="sxs-lookup"><span data-stu-id="db309-127">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="db309-128">For-lus</span><span class="sxs-lookup"><span data-stu-id="db309-128">For loop</span></span>

<span data-ttu-id="db309-129">De `for` instructie ondersteunt herhalingen over een bereik met gehele getallen of een matrix.</span><span class="sxs-lookup"><span data-stu-id="db309-129">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="db309-130">De instructie bestaat uit het tref woord `for` , gevolgd door een symbool of symbool tuple, het tref woord `in` en een expressie van het type `Range` of de matrix, alle tussen haakjes en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="db309-130">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="db309-131">Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met het gedefinieerde symbool (de variabele lus) dat is gekoppeld aan elke waarde in het bereik of de matrix.</span><span class="sxs-lookup"><span data-stu-id="db309-131">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="db309-132">Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="db309-132">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="db309-133">De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus actief is.</span><span class="sxs-lookup"><span data-stu-id="db309-133">The expression is fully evaluated before entering the loop, and does not change while the loop is running.</span></span>

<span data-ttu-id="db309-134">De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en is aan het einde van de hoofd tekst losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="db309-134">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="db309-135">De lus-variabele is niet gebonden nadat de for-lus is voltooid.</span><span class="sxs-lookup"><span data-stu-id="db309-135">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="db309-136">De binding van de lus-variabele is onveranderbaar en volgt dezelfde regels als andere variabele bindingen.</span><span class="sxs-lookup"><span data-stu-id="db309-136">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="db309-137">In deze voor beelden `qubits` is een REGI ster van qubits (bijvoorbeeld type `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="db309-137">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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

<span data-ttu-id="db309-138">Houd er rekening mee dat aan het einde de reken kundige-Shift-Left-operator wordt gebruikt `<<<` .</span><span class="sxs-lookup"><span data-stu-id="db309-138">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="db309-139">Zie [numerieke expressies](xref:microsoft.quantum.guide.expressions#numeric-expressions)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="db309-139">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="db309-140">Herhalen-tot-succes-lus</span><span class="sxs-lookup"><span data-stu-id="db309-140">Repeat-until-success loop</span></span>

<span data-ttu-id="db309-141">De Q# taal maakt de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.</span><span class="sxs-lookup"><span data-stu-id="db309-141">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="db309-142">Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="db309-142">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="db309-143">Voor beelden hiervan zijn de patroon *herhalingen tot geslaagd* (RUS) in Q# .</span><span class="sxs-lookup"><span data-stu-id="db309-143">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="db309-144">Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben. de gefactureerde kosten zijn afhankelijk van de daad werkelijke uitvoering en de interleaving van de meerdere mogelijke vertakkingen.</span><span class="sxs-lookup"><span data-stu-id="db309-144">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="db309-145">Voor het vereenvoudigen van herhaalde tot geslaagde patronen (RUS) worden Q# de constructs ondersteund</span><span class="sxs-lookup"><span data-stu-id="db309-145">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="db309-146">waar `expression` is een geldige expressie die resulteert in een waarde van het type `Bool` .</span><span class="sxs-lookup"><span data-stu-id="db309-146">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="db309-147">De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="db309-147">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="db309-148">Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.</span><span class="sxs-lookup"><span data-stu-id="db309-148">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="db309-149">Alle drie delen van een RUS-lus (de hoofd tekst, de test en de reparatie) worden beschouwd als één bereik *voor elke herhaling*, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in zowel de test als de reparatie.</span><span class="sxs-lookup"><span data-stu-id="db309-149">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="db309-150">Het volt ooien van de uitvoering van de reparatie beëindigt echter het bereik voor de instructie, zodat symbool bindingen die zijn gemaakt in de hoofd tekst of de reparatie, niet beschikbaar zijn in volgende herhalingen.</span><span class="sxs-lookup"><span data-stu-id="db309-150">However, completing the run of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="db309-151">Verder is de `fixup` instructie vaak handig, maar niet altijd nodig.</span><span class="sxs-lookup"><span data-stu-id="db309-151">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="db309-152">In gevallen dat het niet nodig is, de construct</span><span class="sxs-lookup"><span data-stu-id="db309-152">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="db309-153">is ook een geldig RUS-patroon.</span><span class="sxs-lookup"><span data-stu-id="db309-153">is also a valid RUS pattern.</span></span>

<span data-ttu-id="db309-154">Zie voor meer voor beelden en Details [herhalen](#repeat-until-success-examples) in dit artikel.</span><span class="sxs-lookup"><span data-stu-id="db309-154">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="db309-155">Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions.</span><span class="sxs-lookup"><span data-stu-id="db309-155">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="db309-156">Gebruik *while* -lussen om de bijbehorende functionaliteit binnen functions te bieden.</span><span class="sxs-lookup"><span data-stu-id="db309-156">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="db309-157">While-lus</span><span class="sxs-lookup"><span data-stu-id="db309-157">While loop</span></span>

<span data-ttu-id="db309-158">Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation.</span><span class="sxs-lookup"><span data-stu-id="db309-158">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="db309-159">Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, in het bijzonder de exclusieve taal in Q# .</span><span class="sxs-lookup"><span data-stu-id="db309-159">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="db309-160">Als er echter lussen zijn op basis van een voor waarde en de Run-length dus onbekend is tijdens de compilatie, worden deze behandeld met een speciale Care in een Quantum runtime.</span><span class="sxs-lookup"><span data-stu-id="db309-160">However, loops that break based on a condition and whose run length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="db309-161">Hun gebruik in functions is echter ongevoelig omdat deze lussen alleen code bevatten die wordt uitgevoerd op conventionele hardware (niet-Quantum).</span><span class="sxs-lookup"><span data-stu-id="db309-161">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="db309-162">Q#Daarom biedt ondersteuning voor het gebruik van while-lussen in-functies.</span><span class="sxs-lookup"><span data-stu-id="db309-162">Q#, therefore, supports to use of while loops within functions only.</span></span>
<span data-ttu-id="db309-163">Een `while` instructie bestaat uit het tref woord `while` , een Boole-expressie tussen haakjes en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="db309-163">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="db309-164">Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd `true` .</span><span class="sxs-lookup"><span data-stu-id="db309-164">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="conjugations"></a><span data-ttu-id="db309-165">Conjugations</span><span class="sxs-lookup"><span data-stu-id="db309-165">Conjugations</span></span>

<span data-ttu-id="db309-166">In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn.</span><span class="sxs-lookup"><span data-stu-id="db309-166">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="db309-167">Deze effecten kunnen worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="db309-167">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="db309-168">Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende:</span><span class="sxs-lookup"><span data-stu-id="db309-168">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="db309-169">Q# ondersteunt een conjugation-instructie waarmee de voor gaande trans formatie wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="db309-169">Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="db309-170">Met deze instructie kan de bewerking `ApplyWith` op de volgende manier worden geïmplementeerd:</span><span class="sxs-lookup"><span data-stu-id="db309-170">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="db309-171">Een dergelijke conjugation-instructie wordt nuttig als de buiten-en binnenste trans formaties niet direct beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies.</span><span class="sxs-lookup"><span data-stu-id="db309-171">Such a conjugation statement becomes useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="db309-172">De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid.</span><span class="sxs-lookup"><span data-stu-id="db309-172">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="db309-173">Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok.</span><span class="sxs-lookup"><span data-stu-id="db309-173">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="return-statement"></a><span data-ttu-id="db309-174">Instructie return</span><span class="sxs-lookup"><span data-stu-id="db309-174">Return Statement</span></span>

<span data-ttu-id="db309-175">De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="db309-175">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="db309-176">Het bestaat uit het tref woord `return` , gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="db309-176">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="db309-177">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="db309-177">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="db309-178">of</span><span class="sxs-lookup"><span data-stu-id="db309-178">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="db309-179">Een aanroepable die een lege tuple retourneert, `()` heeft geen instructie return nodig.</span><span class="sxs-lookup"><span data-stu-id="db309-179">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="db309-180">Als u een vroege afsluiting van de bewerking of functie wilt opgeven, gebruikt u `return ();` .</span><span class="sxs-lookup"><span data-stu-id="db309-180">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="db309-181">Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.</span><span class="sxs-lookup"><span data-stu-id="db309-181">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="db309-182">Er is geen maximum aantal retour instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="db309-182">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="db309-183">De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="db309-183">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="db309-184">Fout instructie</span><span class="sxs-lookup"><span data-stu-id="db309-184">Fail statement</span></span>

<span data-ttu-id="db309-185">De instructie Fail beëindigt het uitvoeren van een bewerking en retourneert een fout waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="db309-185">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="db309-186">Het bevat het tref woord `fail` , gevolgd door een teken reeks en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="db309-186">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="db309-187">De instructie retourneert de teken reeks naar het klassieke stuur programma als het fout bericht.</span><span class="sxs-lookup"><span data-stu-id="db309-187">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="db309-188">Er is geen beperking voor het aantal mislukte instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="db309-188">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="db309-189">De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="db309-189">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="db309-190">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="db309-190">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="db309-191">of, met behulp van [geïnterpoleerde teken reeksen](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="db309-191">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="db309-192">Herhalen-tot-geslaagde voor beelden</span><span class="sxs-lookup"><span data-stu-id="db309-192">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="db309-193">RUS-patroon voor Qubit draaiing over een Irrational-as</span><span class="sxs-lookup"><span data-stu-id="db309-193">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="db309-194">In een typische use-case Q# implementeert de volgende bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt {5} $ op de Bloch-bol.</span><span class="sxs-lookup"><span data-stu-id="db309-194">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="db309-195">De implementatie maakt gebruik van een bekend RUS-patroon:</span><span class="sxs-lookup"><span data-stu-id="db309-195">The implementation uses a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="db309-196">RUS-lus met een onveranderlijke variabele in het bereik</span><span class="sxs-lookup"><span data-stu-id="db309-196">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="db309-197">In dit voor beeld ziet u het gebruik van een onveranderlijke variabele, `finished` die binnen het bereik van de volledige herhaling-until-reupdate-lus ligt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.</span><span class="sxs-lookup"><span data-stu-id="db309-197">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="db309-198">RUS zonder `fixup`</span><span class="sxs-lookup"><span data-stu-id="db309-198">RUS without `fixup`</span></span>

<span data-ttu-id="db309-199">In dit voor beeld ziet u een RUS-lus zonder de stap voor de reparatie.</span><span class="sxs-lookup"><span data-stu-id="db309-199">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="db309-200">De code is een Probabilistic-circuit dat een belang rijke rotatie poort implementeert $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ met behulp van de- `H` en- `T` poorten.</span><span class="sxs-lookup"><span data-stu-id="db309-200">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="db309-201">De lus eindigt op gemiddeld $ \frac {8} {5} $ herhalingen.</span><span class="sxs-lookup"><span data-stu-id="db309-201">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="db309-202">Zie [*herhalen-tot-geslaagd: niet-deterministische ontleding van single-Qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick en Svore, 2014) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="db309-202">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="db309-203">RUS om een Quantum status voor te bereiden</span><span class="sxs-lookup"><span data-stu-id="db309-203">RUS to prepare a quantum state</span></span>

<span data-ttu-id="db309-204">Ten slotte is hier een voor beeld van een RUS-patroon voor het voorbereiden van een Quantum status $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, te beginnen bij de status $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="db309-204">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="db309-205">Belang rijke programmeer functies die in deze bewerking worden weer gegeven, zijn:</span><span class="sxs-lookup"><span data-stu-id="db309-205">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="db309-206">Een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen betrokken zijn.</span><span class="sxs-lookup"><span data-stu-id="db309-206">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="db309-207">Het gebruik van `AssertMeasurementProbability` instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="db309-207">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="db309-208">[`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) Zie [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging)voor meer informatie over de-en-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="db309-208">For more information about the [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertMeasurementProbability(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertMeasurementProbability(
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

<span data-ttu-id="db309-209">Voor meer informatie, zie voor [beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="db309-209">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="db309-210">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="db309-210">Next steps</span></span>

<span data-ttu-id="db309-211">Meer informatie over [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging) in Q# .</span><span class="sxs-lookup"><span data-stu-id="db309-211">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
