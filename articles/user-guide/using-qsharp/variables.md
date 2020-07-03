---
title: 'Variabelen in Q #'
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 08301f408dcb2211ba25c582a5e5aa43310b714a
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885287"
---
# <a name="variables-in-q"></a><span data-ttu-id="551ea-103">Variabelen in Q #</span><span class="sxs-lookup"><span data-stu-id="551ea-103">Variables in Q#</span></span>

<span data-ttu-id="551ea-104">Q # onderscheidt tussen onveranderlijke en onveranderlijke symbolen, of *variabelen*, die gebonden zijn/toegewezen aan expressies.</span><span class="sxs-lookup"><span data-stu-id="551ea-104">Q# distinguishes between mutable and immutable symbols, or *variables*, which are bound/assigned to expressions.</span></span>
<span data-ttu-id="551ea-105">In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="551ea-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="551ea-106">De linkerkant van een binding bestaat uit een symbool-tuple en de rechter kant van een expressie.</span><span class="sxs-lookup"><span data-stu-id="551ea-106">The left-hand-side of a binding consists of a symbol tuple and the right-hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="551ea-107">Onveranderbare variabelen</span><span class="sxs-lookup"><span data-stu-id="551ea-107">Immutable Variables</span></span>

<span data-ttu-id="551ea-108">U kunt een waarde van elk type in Q # toewijzen aan een variabele voor hergebruik in een bewerking of functie met behulp van het `let` sleutel woord.</span><span class="sxs-lookup"><span data-stu-id="551ea-108">You can assign a value of any type in Q# to a variable for reuse within an operation or function by using the `let` keyword.</span></span> 

<span data-ttu-id="551ea-109">Een onveranderlijke binding bestaat uit het tref woord `let` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen moeten worden verbonden en een punt komma als scheidings teken.</span><span class="sxs-lookup"><span data-stu-id="551ea-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="551ea-110">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="551ea-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="551ea-111">Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan de naam van de variabele (of het symbool), `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="551ea-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="551ea-112">In het vorige voor beeld is het niet nodig expliciet het type van de nieuwe variabele op te geven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en de compiler het juiste type afleidt.</span><span class="sxs-lookup"><span data-stu-id="551ea-112">In the previous example, there is no need to explicitly specify the type of the new variable, as the expression on the right-hand side of the `let` statement is unambiguous, and the compiler infers the correct type.</span></span> 

<span data-ttu-id="551ea-113">Variabelen die zijn gedefinieerd met kunnen `let` *onveranderbaar*zijn, wat inhoudt dat u deze niet meer kunt wijzigen wanneer u deze hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="551ea-113">Variables defined using `let` are *immutable*, meaning that once you define it, you can no longer change it in any way.</span></span>
<span data-ttu-id="551ea-114">Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die op variabelen wordt toegepast voor het Toep assen `Adjoint` van de variant van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="551ea-114">This allows for several beneficial optimizations, including optimization of the classical logic that acts on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="551ea-115">Onveranderlijke variabelen</span><span class="sxs-lookup"><span data-stu-id="551ea-115">Mutable Variables</span></span>

<span data-ttu-id="551ea-116">Als alternatief voor het maken van een variabele met `let` , `mutable` maakt het sleutel woord een onveranderlijke variabele die na de eerste keer dat deze is gemaakt met behulp van het sleutel woord, *kan* worden ontbonden `set` .</span><span class="sxs-lookup"><span data-stu-id="551ea-116">As an alternative to creating a variable with `let`, the `mutable` keyword creates a mutable variable that *can* be rebound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="551ea-117">U kunt symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie opnieuw koppelen aan een andere waarde verderop in de code.</span><span class="sxs-lookup"><span data-stu-id="551ea-117">You can rebind symbols declared and bound as part of a `mutable` statement to a different value later in the code.</span></span> <span data-ttu-id="551ea-118">Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de zojuist gekoppelde waarde compatibel zijn met dat type.</span><span class="sxs-lookup"><span data-stu-id="551ea-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value must be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="551ea-119">Rebinding van onveranderlijke symbolen</span><span class="sxs-lookup"><span data-stu-id="551ea-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="551ea-120">U kunt een onveranderlijke variabele opnieuw binden met behulp van een `set` instructie.</span><span class="sxs-lookup"><span data-stu-id="551ea-120">You can rebind a mutable variable using a `set` statement.</span></span>
<span data-ttu-id="551ea-121">Een herbinding bestaat uit het tref woord `set` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="551ea-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="551ea-122">Hier volgen enkele voor beelden van methoden voor het opnieuw binden van een instructie.</span><span class="sxs-lookup"><span data-stu-id="551ea-122">The following are some examples of rebinding statement techniques.</span></span>

#### <a name="apply-and-reassign-statements"></a><span data-ttu-id="551ea-123">Instructies Toep assen en opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="551ea-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="551ea-124">Een bepaald type `set` instructie, de instructie *Apply-and-reassign* , biedt een handige manier om samen te voegen als de rechter kant de toepassing van een binaire operator is en het resultaat moet worden gekoppeld aan het argument links voor de operator.</span><span class="sxs-lookup"><span data-stu-id="551ea-124">A particular kind of `set`-statement, the *apply-and-reassign* statement, provides a convenient way of concatenation if the right-hand side consists of the application of a binary operator, and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="551ea-125">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="551ea-125">For example,</span></span>

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="551ea-126">verhoogt de waarde van het prestatie meter item `counter` in elke herhaling van de `for` lus.</span><span class="sxs-lookup"><span data-stu-id="551ea-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="551ea-127">De vorige code is gelijk aan</span><span class="sxs-lookup"><span data-stu-id="551ea-127">The previous code is equivalent to</span></span> 

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="551ea-128">Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant overeenkomt met het expressie type.</span><span class="sxs-lookup"><span data-stu-id="551ea-128">Similar statements are available for all binary operators in which the type of the left-hand side matches the expression type.</span></span> <span data-ttu-id="551ea-129">Deze instructies bieden een handige manier om waarden samen te voegen.</span><span class="sxs-lookup"><span data-stu-id="551ea-129">These statements provide a convenient way to accumulate values.</span></span>

<span data-ttu-id="551ea-130">Supposing `qubits` is bijvoorbeeld een REGI ster van qubits:</span><span class="sxs-lookup"><span data-stu-id="551ea-130">For example, supposing `qubits` is a register of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

#### <a name="update-and-reassign-statements"></a><span data-ttu-id="551ea-131">Instructies bijwerken en opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="551ea-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="551ea-132">Er bestaat een soort gelijke samen voeging voor de [expressies voor kopiëren en bijwerken](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="551ea-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand side.</span></span>
<span data-ttu-id="551ea-133">Daarnaast bestaan er instructies voor *bijwerken en opnieuw toewijzen* voor *benoemde items* in door de gebruiker gedefinieerde typen en voor *matrix items*.</span><span class="sxs-lookup"><span data-stu-id="551ea-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="551ea-134">In het geval van matrices [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) beschikt u in de standaard bibliotheek van Q # over de benodigde hulpprogram ma's voor veel algemene matrix initialisatie en bewerkings behoeften. zo voor komt u dat u de matrix items in de eerste plaats hoeft bij te werken.</span><span class="sxs-lookup"><span data-stu-id="551ea-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in the Q# standard library provides the necessary tools for many common array initialization and manipulation needs, and thus helps avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="551ea-135">Instructies update-en-reassign bieden een alternatief als dat nodig is:</span><span class="sxs-lookup"><span data-stu-id="551ea-135">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

<span data-ttu-id="551ea-136">Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , kunt u bijvoorbeeld eenvoudig een functie definiëren die een matrix van `Pauli` typen retourneert waarbij het element op index `i` een gegeven `Pauli` waarde krijgt en alle andere vermeldingen de identiteit () zijn `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="551ea-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), you can, for example, easily define a function that returns an array of `Pauli` types where the element at index `i` takes a given `Pauli` value, and all other entries are the identity (`PauliI`).</span></span>

<span data-ttu-id="551ea-137">Hier vindt u twee definities van een dergelijke functie, met het tweede gebruik van de hulpprogram ma's voor onze afstoting.</span><span class="sxs-lookup"><span data-stu-id="551ea-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli if index==location and PauliI if not
    }    
    return pauliArray;
}
```

<span data-ttu-id="551ea-138">In plaats van elke index in de matrix te herhalen en deze voorwaardelijk in te stellen op `PauliI` of de opgegeven `pauli` , kunt u in plaats daarvan `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) een matrix van `PauliI` typen maken en vervolgens gewoon een kopie-en-update-expressie retour neren waarin u de specifieke waarde op index hebt gewijzigd `location` :</span><span class="sxs-lookup"><span data-stu-id="551ea-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or the given `pauli`, you can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI` types, and then simply return a copy-and-update expression in which you've changed the specific value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="551ea-139">Ontbouw van tuple</span><span class="sxs-lookup"><span data-stu-id="551ea-139">Tuple Deconstruction</span></span>

<span data-ttu-id="551ea-140">Naast het toewijzen van één variabele kunt u de `let` `mutable` sleutel woorden en of een andere bindings constructie gebruiken, zoals `set` -om de inhoud van een [tuple-type](xref:microsoft.quantum.guide.types#tuple-types)uit te pakken.</span><span class="sxs-lookup"><span data-stu-id="551ea-140">In addition to assigning a single variable, you can use the `let` and `mutable` keywords - or any other binding construct, such as `set` - to unpack the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="551ea-141">Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .</span><span class="sxs-lookup"><span data-stu-id="551ea-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="551ea-142">Als de rechter kant van de binding een tuple is, kunt u die tupel tijdens toewijzing ontkoppelen.</span><span class="sxs-lookup"><span data-stu-id="551ea-142">If the right-hand side of the binding is a tuple, then you can deconstruct that tuple upon assignment.</span></span>
<span data-ttu-id="551ea-143">Deze ontbouwingen kunnen gebruikmaken van geneste Tuples en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.</span><span class="sxs-lookup"><span data-stu-id="551ea-143">Such deconstructions can involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right-hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="551ea-144">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="551ea-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="551ea-145">Bindings bereiken</span><span class="sxs-lookup"><span data-stu-id="551ea-145">Binding Scopes</span></span>

<span data-ttu-id="551ea-146">Over het algemeen gaan symbool bindingen zich buiten het bereik en worden ze niet meer aan het einde van het instructie blok weer gegeven waarin ze zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="551ea-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="551ea-147">Er zijn twee uitzonde ringen op deze regel:</span><span class="sxs-lookup"><span data-stu-id="551ea-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="551ea-148">De binding van de lus-variabele van een `for` lus bevindt zich in het bereik voor de hoofd tekst van de lus for, maar niet na het einde van de lus.</span><span class="sxs-lookup"><span data-stu-id="551ea-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="551ea-149">Alle drie delen van een `repeat` / `until` lus (de hoofd tekst, de test en de reparatie) fungeren als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en de reparatie.</span><span class="sxs-lookup"><span data-stu-id="551ea-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) act as a single scope, so symbols that are bound in the body are available in the test and the fixup.</span></span>

<span data-ttu-id="551ea-150">Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen vanuit een eerdere fase niet meer beschikbaar zijn in een latere fase.</span><span class="sxs-lookup"><span data-stu-id="551ea-150">For both types of loops, each pass through the loop runs in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="551ea-151">Zie [controle stroom](xref:microsoft.quantum.guide.controlflow)voor meer informatie over deze lussen.</span><span class="sxs-lookup"><span data-stu-id="551ea-151">For more information on these loops, see [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="551ea-152">Binnenste blokken nemen symbool bindingen over van de buitenste blokken.</span><span class="sxs-lookup"><span data-stu-id="551ea-152">Inner blocks inherit symbol bindings from outer blocks.</span></span>
<span data-ttu-id="551ea-153">U kunt slechts eenmaal per blok een symbool binden; het is niet toegestaan om een symbool te definiëren met dezelfde naam als een ander symbool dat zich binnen het bereik bevindt (geen "schaduw").</span><span class="sxs-lookup"><span data-stu-id="551ea-153">You can only bind a symbol once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="551ea-154">De volgende reeksen zijn geldig:</span><span class="sxs-lookup"><span data-stu-id="551ea-154">The following sequences are legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="551ea-155">en</span><span class="sxs-lookup"><span data-stu-id="551ea-155">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

<span data-ttu-id="551ea-156">Maar dit is niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="551ea-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="551ea-157">Zo zou:</span><span class="sxs-lookup"><span data-stu-id="551ea-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a><span data-ttu-id="551ea-158">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="551ea-158">Next steps</span></span>

<span data-ttu-id="551ea-159">Meer informatie over het [werken met qubits](xref:microsoft.quantum.guide.qubits) in Q #.</span><span class="sxs-lookup"><span data-stu-id="551ea-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>