---
title: 'Variabelen in Q #'
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 407b4ff3570816eb7bdc323a5c5b77dac2d951af
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430897"
---
# <a name="variables-in-q"></a><span data-ttu-id="22b1c-103">Variabelen in Q #</span><span class="sxs-lookup"><span data-stu-id="22b1c-103">Variables in Q#</span></span>

<span data-ttu-id="22b1c-104">Q # onderscheidt tussen onveranderlijke en onveranderlijke symbolen, of ' variabelen ', die gebonden zijn/toegewezen aan expressies.</span><span class="sxs-lookup"><span data-stu-id="22b1c-104">Q# distinguishes between mutable and immutable symbols, or "variables", which are bound/assigned to expressions.</span></span>
<span data-ttu-id="22b1c-105">In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="22b1c-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="22b1c-106">De linkerkant van een binding bestaat uit een symbool-tuple en de rechter kant van een expressie.</span><span class="sxs-lookup"><span data-stu-id="22b1c-106">The left-hand-side of a binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="22b1c-107">Onveranderbare variabelen</span><span class="sxs-lookup"><span data-stu-id="22b1c-107">Immutable Variables</span></span>

<span data-ttu-id="22b1c-108">Een waarde van elk type in Q # kan worden toegewezen aan een variabele voor hergebruik in een bewerking of functie met behulp van het `let` sleutel woord.</span><span class="sxs-lookup"><span data-stu-id="22b1c-108">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>

<span data-ttu-id="22b1c-109">Een onveranderlijke binding bestaat uit het tref woord `let` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen moeten worden verbonden en een punt komma als scheidings teken.</span><span class="sxs-lookup"><span data-stu-id="22b1c-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="22b1c-110">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="22b1c-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="22b1c-111">Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan de naam van de variabele (of het symbool), `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="22b1c-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="22b1c-112">We hoeven het type van de nieuwe variabele niet expliciet op te geven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en het type wordt afgeleid door de compiler.</span><span class="sxs-lookup"><span data-stu-id="22b1c-112">We did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="22b1c-113">Variabelen die zijn gedefinieerd met kunnen `let` *onveranderbaar*zijn, wat betekent dat wanneer deze eenmaal is gedefinieerd, deze niet meer op een wille keurige manier kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="22b1c-113">Variables defined using `let` are *immutable*, meaning that once it has been defined, it can no longer be changed in any way.</span></span>
<span data-ttu-id="22b1c-114">Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die wordt toegepast op variabelen voor het Toep assen `Adjoint` van de variant van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="22b1c-114">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="22b1c-115">Onveranderlijke variabelen</span><span class="sxs-lookup"><span data-stu-id="22b1c-115">Mutable Variables</span></span>

<span data-ttu-id="22b1c-116">Als alternatief voor het maken van een variabele met wordt met `let` het `mutable` tref woord een onveranderlijke variabele gemaakt die opnieuw *kan* worden gebonden nadat deze in eerste instantie is gemaakt met behulp van het `set` sleutel woord.</span><span class="sxs-lookup"><span data-stu-id="22b1c-116">As an alternative to creating a variable with `let`, the `mutable` keyword will create a mutable variable that *can* be re-bound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="22b1c-117">Symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie, kunnen later in de code opnieuw worden gebonden aan een andere waarde.</span><span class="sxs-lookup"><span data-stu-id="22b1c-117">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> <span data-ttu-id="22b1c-118">Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de zojuist gekoppelde waarde compatibel zijn met dat type.</span><span class="sxs-lookup"><span data-stu-id="22b1c-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="22b1c-119">Rebinding van onveranderlijke symbolen</span><span class="sxs-lookup"><span data-stu-id="22b1c-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="22b1c-120">Een onveranderlijke variabele kan worden gekoppeld met behulp van een- `set` instructie.</span><span class="sxs-lookup"><span data-stu-id="22b1c-120">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="22b1c-121">Een herbinding bestaat uit het tref woord `set` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="22b1c-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="22b1c-122">Hier bieden we enkele mogelijke voor beelden van de technieken voor het opnieuw binden van een instructie</span><span class="sxs-lookup"><span data-stu-id="22b1c-122">Here, we provide some possible examples of rebinding statement techniques</span></span>

### <a name="apply-and-reassign-statements"></a><span data-ttu-id="22b1c-123">Instructies Toep assen en opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="22b1c-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="22b1c-124">Een bepaalde soort `set` instructie wordt verwezen naar een instructie *Apply-and-reassign, en* biedt een handige manier om samen te voegen als de rechter kant bestaat uit de toepassing van een binaire operator en het resultaat moet worden gekoppeld aan het argument links voor de operator.</span><span class="sxs-lookup"><span data-stu-id="22b1c-124">A particular kind of `set`-statement we refer to as an *apply-and-reassign* statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="22b1c-125">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="22b1c-125">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="22b1c-126">verhoogt de waarde van het prestatie meter item `counter` in elke herhaling van de `for` lus.</span><span class="sxs-lookup"><span data-stu-id="22b1c-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="22b1c-127">De bovenstaande code is gelijk aan</span><span class="sxs-lookup"><span data-stu-id="22b1c-127">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="22b1c-128">Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant van het expressie type overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="22b1c-128">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="22b1c-129">Dit biedt bijvoorbeeld een handige manier om waarden te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="22b1c-129">This provides for example a convenient way to accumulate values.</span></span>

<span data-ttu-id="22b1c-130">Supposing `qubits` is bijvoorbeeld een regsiter van qubits:</span><span class="sxs-lookup"><span data-stu-id="22b1c-130">For example, supposing `qubits` is a regsiter of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a><span data-ttu-id="22b1c-131">Instructies bijwerken en opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="22b1c-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="22b1c-132">Er bestaat een soort gelijke samen voeging voor [expressies voor kopiëren en bijwerken](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="22b1c-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand-side.</span></span>
<span data-ttu-id="22b1c-133">Daarnaast bestaan er instructies voor *bijwerken en opnieuw toewijzen* voor *benoemde items* in door de gebruiker gedefinieerde typen en voor *matrix items*.</span><span class="sxs-lookup"><span data-stu-id="22b1c-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

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

<span data-ttu-id="22b1c-134">In het geval van matrices [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) biedt de standaard bibliotheken de benodigde hulpprogram ma's voor veel algemene matrix initialisatie-en bewerkings behoeften. zo voor komt u dat u matrix items in de eerste plaats hoeft bij te werken.</span><span class="sxs-lookup"><span data-stu-id="22b1c-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in our standard libraries provides the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="22b1c-135">Instructies update-en-reassign bieden een alternatief als dat nodig is:</span><span class="sxs-lookup"><span data-stu-id="22b1c-135">Update-and-reassign statements provide an alternative if needed:</span></span>

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

<span data-ttu-id="22b1c-136">Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , kunnen we bijvoorbeeld eenvoudig een functie definiëren die een matrix van PAULIS retourneert waarbij de Pauli bij index `i` de opgegeven waarde krijgt en alle andere vermeldingen de identiteit zijn.</span><span class="sxs-lookup"><span data-stu-id="22b1c-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can, for example, easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity.</span></span>

<span data-ttu-id="22b1c-137">Hier vindt u twee definities van een dergelijke functie, met het tweede gebruik van de hulpprogram ma's voor onze afstoting.</span><span class="sxs-lookup"><span data-stu-id="22b1c-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

<span data-ttu-id="22b1c-138">In plaats van elke index in de matrix te herhalen en het beleid voorwaardelijk in te stellen op `PauliI` of `Pauli` , kunnen we in plaats daarvan een `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) matrix van maken `PauliI` en vervolgens gewoon een kopie-en-update-expressie retour neren waarin we de specifc-waarde bij index hebben gewijzigd `location` :</span><span class="sxs-lookup"><span data-stu-id="22b1c-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or `Pauli`, we can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI`'s, and then simply returning a copy-and-update expression in which we've changed the specifc value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="22b1c-139">Ontbouw van tuple</span><span class="sxs-lookup"><span data-stu-id="22b1c-139">Tuple Deconstruction</span></span>

<span data-ttu-id="22b1c-140">Naast het toewijzen van één variabele, de `let` `mutable` sleutel woorden---of in feite een andere bindings constructie, zoals `set` (hieronder beschreven)---kunt u ook de inhoud van een [tuple-type](xref:microsoft.quantum.guide.types#tuple-types)uitpakken.</span><span class="sxs-lookup"><span data-stu-id="22b1c-140">In addition to assigning a single variable, the `let` and `mutable` keywords---or in fact any other binding construct, such as `set` (described below)---also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="22b1c-141">Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .</span><span class="sxs-lookup"><span data-stu-id="22b1c-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="22b1c-142">Als de rechter kant van de binding een tuple is, kan die tuple worden ontbouwd bij toewijzing.</span><span class="sxs-lookup"><span data-stu-id="22b1c-142">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="22b1c-143">Deze ontbouwingen kunnen geneste Tuples omvatten en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.</span><span class="sxs-lookup"><span data-stu-id="22b1c-143">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="22b1c-144">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="22b1c-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="22b1c-145">Bindings bereiken</span><span class="sxs-lookup"><span data-stu-id="22b1c-145">Binding Scopes</span></span>

<span data-ttu-id="22b1c-146">Over het algemeen gaan symbool bindingen zich buiten het bereik en worden ze niet meer aan het einde van het instructie blok weer gegeven waarin ze zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="22b1c-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="22b1c-147">Er zijn twee uitzonde ringen op deze regel:</span><span class="sxs-lookup"><span data-stu-id="22b1c-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="22b1c-148">De binding van de lus-variabele van een `for` lus bevindt zich in het bereik voor de hoofd tekst van de lus for, maar niet na het einde van de lus.</span><span class="sxs-lookup"><span data-stu-id="22b1c-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="22b1c-149">Alle drie delen van een `repeat` / `until` lus (de hoofd tekst, de test en de reparatie) worden behandeld als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en in de reparatie.</span><span class="sxs-lookup"><span data-stu-id="22b1c-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="22b1c-150">Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen van een eerdere Passes niet meer beschikbaar zijn in een latere fase.</span><span class="sxs-lookup"><span data-stu-id="22b1c-150">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="22b1c-151">Meer informatie over deze lussen vindt u in de [controle stroom](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="22b1c-151">Details on these loops can be found at [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="22b1c-152">Symbool bindingen van de buitenste blokken worden overgenomen door binnenste blokken.</span><span class="sxs-lookup"><span data-stu-id="22b1c-152">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="22b1c-153">Een symbool mag slechts eenmaal per blok zijn gebonden; het is niet toegestaan om een symbool te definiëren met dezelfde naam als een ander symbool dat zich binnen het bereik bevindt (geen "schaduw").</span><span class="sxs-lookup"><span data-stu-id="22b1c-153">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="22b1c-154">De volgende reeksen zijn juridisch:</span><span class="sxs-lookup"><span data-stu-id="22b1c-154">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="22b1c-155">en</span><span class="sxs-lookup"><span data-stu-id="22b1c-155">and</span></span>

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

<span data-ttu-id="22b1c-156">Maar dit is niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="22b1c-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="22b1c-157">Zo zou:</span><span class="sxs-lookup"><span data-stu-id="22b1c-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="whats-next"></a><span data-ttu-id="22b1c-158">Hoe nu verder?</span><span class="sxs-lookup"><span data-stu-id="22b1c-158">What's Next?</span></span>
<span data-ttu-id="22b1c-159">Meer informatie over het [werken met qubits](xref:microsoft.quantum.guide.qubits) in Q #.</span><span class="sxs-lookup"><span data-stu-id="22b1c-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>