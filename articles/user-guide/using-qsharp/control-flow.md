---
title: 'Controle stroom in Q #'
description: Lussen, voor waarden enzovoort.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: c534e016fcb8b50e66c11ca29c253ba0512acc6e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430948"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="c1e75-103">Controle stroom in Q #</span><span class="sxs-lookup"><span data-stu-id="c1e75-103">Control Flow in Q#</span></span>

<span data-ttu-id="c1e75-104">Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met de meest voorkomende verplichte klassieke talen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-104">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="c1e75-105">Deze controle stroom kan echter op drie verschillende manieren worden gewijzigd:</span><span class="sxs-lookup"><span data-stu-id="c1e75-105">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="c1e75-106">`if`instructies</span><span class="sxs-lookup"><span data-stu-id="c1e75-106">`if` statements</span></span>
- <span data-ttu-id="c1e75-107">`for`lussen</span><span class="sxs-lookup"><span data-stu-id="c1e75-107">`for` loops</span></span>
- <span data-ttu-id="c1e75-108">`repeat`-`until`lussen</span><span class="sxs-lookup"><span data-stu-id="c1e75-108">`repeat`-`until` loops</span></span>

<span data-ttu-id="c1e75-109">We stellen de bespreking van de laatste uit [voor meer informatie](#repeat-until-success-loop).</span><span class="sxs-lookup"><span data-stu-id="c1e75-109">We defer discussion of the latter to further [below](#repeat-until-success-loop).</span></span>
<span data-ttu-id="c1e75-110">De `if` `for` constructies en de controle stroom kunnen echter door gaan in een vertrouwde zin voor de meeste klassieke programmeer talen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-110">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>

<span data-ttu-id="c1e75-111">Belang rijk: `for` lussen en `if` instructies kunnen zelfs worden gebruikt in bewerkingen waarvoor specials automatisch worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-111">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="c1e75-112">In dat geval keert de adjoint van een `for` lus de richting om en neemt de adjoint van elke iteratie toe.</span><span class="sxs-lookup"><span data-stu-id="c1e75-112">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="c1e75-113">Dit is het principe ' schoenen en SOCKS ': als u het uitvoeren van een SOCKS ongedaan wilt maken en vervolgens schoenen wilt maken, moet u het op schoenen opzetten en vervolgens op SOCKS ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="c1e75-113">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="c1e75-114">Het werkt minder goed om uw SOCKS uit te proberen terwijl u nog steeds uw schoenen afdraagt!</span><span class="sxs-lookup"><span data-stu-id="c1e75-114">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="if-else-if-else"></a><span data-ttu-id="c1e75-115">If, else-if, else</span><span class="sxs-lookup"><span data-stu-id="c1e75-115">If, Else-if, Else</span></span>

<span data-ttu-id="c1e75-116">De `if` instructie ondersteunt voorwaardelijke uitvoering.</span><span class="sxs-lookup"><span data-stu-id="c1e75-116">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="c1e75-117">Het bestaat uit het tref woord `if` , een open haakje, een `(` Boole-expressie, een haakje sluiten `)` en een instructie blok (de _vervolgens_ blok kering).</span><span class="sxs-lookup"><span data-stu-id="c1e75-117">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="c1e75-118">Dit kan worden gevolgd door een wille keurig aantal else-if-componenten, die elk bestaan uit het sleutel woord `elif` , een haakje openen `(` , een booleaanse expressie, een haakje sluiten `)` en een instructie blok (het _else-if-_ blok).</span><span class="sxs-lookup"><span data-stu-id="c1e75-118">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="c1e75-119">Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).</span><span class="sxs-lookup"><span data-stu-id="c1e75-119">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="c1e75-120">De `if` voor waarde wordt geëvalueerd, en als deze waar is, wordt de blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-120">The `if` condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="c1e75-121">Als de voor waarde ONWAAR is, wordt de eerste else-if-voor waarde geëvalueerd; Als de waarde True is, wordt het blok Else-If uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-121">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="c1e75-122">Anders wordt het tweede else-if-blok getest en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.</span><span class="sxs-lookup"><span data-stu-id="c1e75-122">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="c1e75-123">Als de component origineel als voor waarde en alle else-if resulteert in ONWAAR, wordt het else-blok uitgevoerd als er een is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c1e75-123">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="c1e75-124">Houd er rekening mee dat welk blok wordt uitgevoerd in een eigen bereik.</span><span class="sxs-lookup"><span data-stu-id="c1e75-124">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="c1e75-125">Bindingen die zijn gemaakt in een `if` , `elif` of `else` blok zijn niet zichtbaar na het einde.</span><span class="sxs-lookup"><span data-stu-id="c1e75-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after its end.</span></span>

<span data-ttu-id="c1e75-126">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="c1e75-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="c1e75-127">of</span><span class="sxs-lookup"><span data-stu-id="c1e75-127">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="c1e75-128">For-lus</span><span class="sxs-lookup"><span data-stu-id="c1e75-128">For Loop</span></span>

<span data-ttu-id="c1e75-129">De `for` instructie ondersteunt iteratie over een geheel getal of een matrix.</span><span class="sxs-lookup"><span data-stu-id="c1e75-129">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="c1e75-130">De instructie bestaat uit het tref woord `for` , een open haakje, `(` gevolgd door een symbool of symbool tuple, het tref woord `in` , een expressie van het type `Range` of de matrix, een haakje sluiten `)` en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="c1e75-130">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="c1e75-131">Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met de gedefinieerde symbolen (een of meer lussen) die zijn gekoppeld aan elke waarde in het bereik of de matrix.</span><span class="sxs-lookup"><span data-stu-id="c1e75-131">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="c1e75-132">Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-132">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="c1e75-133">De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-133">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="c1e75-134">De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en ontbond aan het einde van de hoofd tekst.</span><span class="sxs-lookup"><span data-stu-id="c1e75-134">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="c1e75-135">Met name de lus-variabele is niet gebonden nadat de for-lus is voltooid.</span><span class="sxs-lookup"><span data-stu-id="c1e75-135">In particular, the loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="c1e75-136">De binding van de gedeclareerde symbolen is onveranderbaar en volgt dezelfde regels als andere variabele bindingen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-136">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="c1e75-137">Voor sommige voor beelden `qubits` is supposing een REGI ster van qubits (bijvoorbeeld type `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="c1e75-137">For some examples, supposing `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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
<span data-ttu-id="c1e75-138">U ziet dat aan het eind de reken kundige-Shift-Left-operator wordt gebruikt, `<<<` Details van die kunnen worden gevonden bij [numerieke expressies](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span><span class="sxs-lookup"><span data-stu-id="c1e75-138">Note that at the end we utilized the arithmetic-shift-left binary operator, `<<<`, details of which can be found at [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span></span>


## <a name="repeat-until-success-loop"></a><span data-ttu-id="c1e75-139">Herhalen-tot-succes-lus</span><span class="sxs-lookup"><span data-stu-id="c1e75-139">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="c1e75-140">De Q #-taal staat de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.</span><span class="sxs-lookup"><span data-stu-id="c1e75-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="c1e75-141">Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-141">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="c1e75-142">Een voor beeld is het eenvoudig om te implementeren, dat wil zeggen, *herhalen-tot-succes-* patronen (RUS) in Q #.</span><span class="sxs-lookup"><span data-stu-id="c1e75-142">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="c1e75-143">Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben, maar waarvoor de werkelijke kosten afhankelijk zijn van een feitelijke uitvoering en een daad werkelijke interleaving van verschillende mogelijke vertakkingen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="c1e75-144">Q # ondersteunt de constructs om herhaalde tot geslaagde patronen (RUS) te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="c1e75-144">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="c1e75-145">waar `expression` is een geldige expressie die resulteert in een waarde van het type `Bool` .</span><span class="sxs-lookup"><span data-stu-id="c1e75-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="c1e75-146">De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-146">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="c1e75-147">Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.</span><span class="sxs-lookup"><span data-stu-id="c1e75-147">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>

<span data-ttu-id="c1e75-148">Alle drie delen van een herhaling/until-lus (de hoofd tekst, de test en de reparatie) worden beschouwd als één bereik *voor elke herhaling*, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en in de reparatie.</span><span class="sxs-lookup"><span data-stu-id="c1e75-148">All three portions of a repeat/until loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in the test and in the fixup.</span></span>
<span data-ttu-id="c1e75-149">Het volt ooien van de uitvoering van de reparatie beëindigt echter het bereik voor de-instructie, zodat symbool bindingen die zijn gemaakt tijdens de hoofd tekst of reparatie, niet beschikbaar zijn in volgende herhalingen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-149">However completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="c1e75-150">Verder is de `fixup` instructie vaak handig, maar niet altijd nodig.</span><span class="sxs-lookup"><span data-stu-id="c1e75-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="c1e75-151">In gevallen dat het niet nodig is, de construct</span><span class="sxs-lookup"><span data-stu-id="c1e75-151">In cases that it is not needed, the construct</span></span>
```qsharp
repeat {
    // do stuff
}
until (expression);
```
<span data-ttu-id="c1e75-152">is ook een geldig RUS-patroon.</span><span class="sxs-lookup"><span data-stu-id="c1e75-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="c1e75-153">Onder aan deze pagina wordt een aantal [voor beelden van Rus-lussen](#repeat-until-success-examples)weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="c1e75-153">At the bottom of this page we present some [examples of RUS loops](#repeat-until-success-examples).</span></span>

> [!TIP]   
> <span data-ttu-id="c1e75-154">Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions.</span><span class="sxs-lookup"><span data-stu-id="c1e75-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="c1e75-155">De bijbehorende functionaliteit wordt gegeven door-lussen in-functies.</span><span class="sxs-lookup"><span data-stu-id="c1e75-155">The corresponding functionality is provided by while loops in functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="c1e75-156">Lus while</span><span class="sxs-lookup"><span data-stu-id="c1e75-156">While Loop</span></span>

<span data-ttu-id="c1e75-157">Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation.</span><span class="sxs-lookup"><span data-stu-id="c1e75-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="c1e75-158">Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, dus de speciale taal construct in Q #.</span><span class="sxs-lookup"><span data-stu-id="c1e75-158">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="c1e75-159">Lussen die op basis van een voor waarde worden uitgevoerd en waarvan de uitvoerings lengte daarom onbekend is tijdens de compilatie, moeten worden behandeld met een speciale Care in een Quantum runtime.</span><span class="sxs-lookup"><span data-stu-id="c1e75-159">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="c1e75-160">Het gebruik ervan in functions is niet probleemend, omdat deze alleen code bevatten die op conventionele hardware (niet-Quantum) wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1e75-160">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="c1e75-161">Q # ondersteunt daarom alleen het gebruik van while-lussen in-functies.</span><span class="sxs-lookup"><span data-stu-id="c1e75-161">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="c1e75-162">Een `while` instructie bestaat uit het tref woord `while` , een open haakje, een `(` voor waarde (bijvoorbeeld een Boole-expressie), een haakje sluiten `)` en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="c1e75-162">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="c1e75-163">Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd `true` .</span><span class="sxs-lookup"><span data-stu-id="c1e75-163">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a><span data-ttu-id="c1e75-164">Instructie return</span><span class="sxs-lookup"><span data-stu-id="c1e75-164">Return Statement</span></span>

<span data-ttu-id="c1e75-165">De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="c1e75-165">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="c1e75-166">Het bestaat uit het tref woord `return` , gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="c1e75-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="c1e75-167">Een aanroepable die een lege tuple retourneert, `()` heeft geen instructie return nodig.</span><span class="sxs-lookup"><span data-stu-id="c1e75-167">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="c1e75-168">Als een vroege afsluiting gewenst is, `return ()` kan in dit geval worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c1e75-168">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="c1e75-169">Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.</span><span class="sxs-lookup"><span data-stu-id="c1e75-169">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="c1e75-170">Er is geen maximum aantal retour instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="c1e75-170">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="c1e75-171">De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-171">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="c1e75-172">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="c1e75-172">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="c1e75-173">of</span><span class="sxs-lookup"><span data-stu-id="c1e75-173">or</span></span>
```qsharp
return ();
```
<span data-ttu-id="c1e75-174">of</span><span class="sxs-lookup"><span data-stu-id="c1e75-174">or</span></span>
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a><span data-ttu-id="c1e75-175">Fout instructie</span><span class="sxs-lookup"><span data-stu-id="c1e75-175">Fail Statement</span></span>

<span data-ttu-id="c1e75-176">De instructie Fail beëindigt de uitvoering van een bewerking en retourneert een fout waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="c1e75-176">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="c1e75-177">Het bevat het tref woord `fail` , gevolgd door een teken reeks en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="c1e75-177">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="c1e75-178">De teken reeks wordt geretourneerd naar het klassieke stuur programma als het fout bericht.</span><span class="sxs-lookup"><span data-stu-id="c1e75-178">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="c1e75-179">Er is geen beperking voor het aantal mislukte instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="c1e75-179">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="c1e75-180">De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-180">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="c1e75-181">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="c1e75-181">For example,</span></span>
```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="c1e75-182">of, met behulp van [geïnterpoleerde teken reeksen](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="c1e75-182">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="c1e75-183">Herhalen-tot-geslaagde voor beelden</span><span class="sxs-lookup"><span data-stu-id="c1e75-183">Repeat-Until-Success Examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="c1e75-184">RUS-patroon voor één Qubit draaiing over een Irrational-as</span><span class="sxs-lookup"><span data-stu-id="c1e75-184">RUS pattern for single qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="c1e75-185">In een typische use-case implementeert de volgende Q #-bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt {5} $ op de Bloch-bol.</span><span class="sxs-lookup"><span data-stu-id="c1e75-185">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="c1e75-186">Dit wordt bereikt door gebruik te maken van een bekend RUS-patroon:</span><span class="sxs-lookup"><span data-stu-id="c1e75-186">This is accomplished by using a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a><span data-ttu-id="c1e75-187">RUS-lus met onveranderlijke variabele in bereik</span><span class="sxs-lookup"><span data-stu-id="c1e75-187">RUS loop with mutable variable in scope</span></span>

<span data-ttu-id="c1e75-188">In dit voor beeld ziet u het gebruik van een onveranderlijke variabele `finished` die zich binnen het bereik van de volledige herhaling-until-reactie-lus bevindt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.</span><span class="sxs-lookup"><span data-stu-id="c1e75-188">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="c1e75-189">RUS zonder`fixup`</span><span class="sxs-lookup"><span data-stu-id="c1e75-189">RUS without `fixup`</span></span>

<span data-ttu-id="c1e75-190">De volgende code is bijvoorbeeld een Probabilistic-circuit waarmee een belang rijke rotatie poort wordt geïmplementeerd $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ met behulp van de `H` en- `T` poorten.</span><span class="sxs-lookup"><span data-stu-id="c1e75-190">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="c1e75-191">De lus eindigt op gemiddeld $ \frac {8} {5} $ herhalingen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="c1e75-192">Zie [*herhalen-tot-geslaagd: niet-deterministische ontleding van single-Qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick en Svore, 2014) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c1e75-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="c1e75-193">RUS om een Quantum status voor te bereiden</span><span class="sxs-lookup"><span data-stu-id="c1e75-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="c1e75-194">Tot slot wordt een voor beeld van een RUS-patroon weer gegeven om een Quantum status te bereiden $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, te beginnen met de status $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="c1e75-194">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="c1e75-195">Zie ook het [voor beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="c1e75-195">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

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

<span data-ttu-id="c1e75-196">Opvallende programmatische functies die in deze bewerking worden weer gegeven, zijn een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen worden uitgevoerd, en het gebruik van `AssertProb` instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="c1e75-196">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="c1e75-197">Zie ook [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging) voor meer informatie over de [`Assert`](xref:microsoft.quantum.intrinsic.assert) en- [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="c1e75-197">See also [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>


## <a name="whats-next"></a><span data-ttu-id="c1e75-198">Hoe nu verder?</span><span class="sxs-lookup"><span data-stu-id="c1e75-198">What's Next?</span></span>
<span data-ttu-id="c1e75-199">Meer informatie over [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging) in Q #.</span><span class="sxs-lookup"><span data-stu-id="c1e75-199">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>