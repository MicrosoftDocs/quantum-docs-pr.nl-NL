---
title: Flow-besturings elementen in de Q# standaard libararies
description: Meer informatie over de bewerkingen en functies voor datatransport besturing in de micro soft- Q# standaard bibliotheek.
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1cfef50cf2bbecd2043972a662edd8120c5570ec
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835618"
---
# <a name="higher-order-control-flow"></a><span data-ttu-id="b6381-103">Controle stroom met hogere volg orde</span><span class="sxs-lookup"><span data-stu-id="b6381-103">Higher-Order Control Flow</span></span> #

<span data-ttu-id="b6381-104">Een van de primaire rollen van de standaard bibliotheek is om het eenvoudiger te maken om zeer belang rijke ideeën in te stellen als [Quantum Program ma's](https://en.wikipedia.org/wiki/Quantum_programming).</span><span class="sxs-lookup"><span data-stu-id="b6381-104">One of the primary roles of the standard library is to make it easier to express high-level algorithmic ideas as [quantum programs](https://en.wikipedia.org/wiki/Quantum_programming).</span></span>
<span data-ttu-id="b6381-105">Daarom Q# biedt Canon diverse verschillende constructies voor datatransport besturing, die allemaal zijn geïmplementeerd met behulp van gedeeltelijke toepassing van functies en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="b6381-105">Thus, the Q# canon provides a variety of different flow control constructs, each implemented using partial application of functions and operations.</span></span>
<span data-ttu-id="b6381-106">Als u direct naar een voor beeld gaat, moet u rekening houden met het geval waarin één ' CNOT ladder ' moet worden gemaakt in een REGI ster:</span><span class="sxs-lookup"><span data-stu-id="b6381-106">Jumping immediately into an example, consider the case in which one wants to construct a "CNOT ladder" on a register:</span></span>

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

<span data-ttu-id="b6381-107">We kunnen dit patroon uitdrukken met behulp van herhalingen en `for` lussen:</span><span class="sxs-lookup"><span data-stu-id="b6381-107">We can express this pattern by using iteration and `for` loops:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

<span data-ttu-id="b6381-108">Uitgedrukt in termen van <xref:microsoft.quantum.canon.applytoeachca> -en array-manipulatie functies <xref:microsoft.quantum.arrays.zip> , zoals, is dit echter veel korter en eenvoudiger te lezen:</span><span class="sxs-lookup"><span data-stu-id="b6381-108">Expressed in terms of <xref:microsoft.quantum.canon.applytoeachca> and array manipulation functions such as <xref:microsoft.quantum.arrays.zip>, however, this is much shorter and easier to read:</span></span>

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

<span data-ttu-id="b6381-109">In de rest van deze sectie bieden we een aantal voor beelden van het gebruik van de verschillende Flow Control-bewerkingen en-functies die door de Canon worden geboden om de Quantum Program ma's te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="b6381-109">In the rest of this section, we will provide a number of examples of how to use the various flow control operations and functions provided by the canon to compactly express quantum programs.</span></span>

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a><span data-ttu-id="b6381-110">Bewerkingen en functies Toep assen op matrices en bereiken</span><span class="sxs-lookup"><span data-stu-id="b6381-110">Applying Operations and Functions over Arrays and Ranges</span></span> ##

<span data-ttu-id="b6381-111">Een van de primaire abstracties van de Canon is die van iteratie.</span><span class="sxs-lookup"><span data-stu-id="b6381-111">One of the primary abstractions provided by the canon is that of iteration.</span></span>
<span data-ttu-id="b6381-112">Denk bijvoorbeeld aan een unitary van het formulier $U \otimes U \otimes \cdots \otimes U $ voor een single-Qubit unitary $U $.</span><span class="sxs-lookup"><span data-stu-id="b6381-112">For instance, consider a unitary of the form $U \otimes U \otimes \cdots \otimes U$ for a single-qubit unitary $U$.</span></span>
<span data-ttu-id="b6381-113">In kunnen Q# we gebruiken <xref:microsoft.quantum.arrays.indexrange> om dit als een `for` lus voor een REGI ster te vertegenwoordigen:</span><span class="sxs-lookup"><span data-stu-id="b6381-113">In Q#, we might use <xref:microsoft.quantum.arrays.indexrange> to represent this as as a `for` loop over a register:</span></span>

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation ApplyHadamardToAll(
    register : Qubit[])
: Unit is Adj + Ctl {
    for (qubit in register) {
        H(qubit);
    }
}
```

<span data-ttu-id="b6381-114">We kunnen deze nieuwe bewerking vervolgens gebruiken `HAll(register)` om $H \Otimes h \otimes \cdots \Otimes h $ toe te passen.</span><span class="sxs-lookup"><span data-stu-id="b6381-114">We can then use this new operation as `HAll(register)` to apply $H \otimes H \otimes \cdots \otimes H$.</span></span>

<span data-ttu-id="b6381-115">Dit is een lastigere, maar met name in een groter algoritme.</span><span class="sxs-lookup"><span data-stu-id="b6381-115">This is cumbersome to do, however, especially in a larger algorithm.</span></span>
<span data-ttu-id="b6381-116">Deze benadering is bovendien gespecialiseerd in de specifieke bewerking die we op elke qubit willen Toep assen.</span><span class="sxs-lookup"><span data-stu-id="b6381-116">Moreover, this approach is specialized to the particular operation that we wish to apply to each qubit.</span></span>
<span data-ttu-id="b6381-117">We kunnen het feit gebruiken dat bewerkingen een eerste klasse zijn om dit algoritmen-concept explicieter te maken:</span><span class="sxs-lookup"><span data-stu-id="b6381-117">We can use the fact that operations are first-class to express this algorithmic concept more explicitly:</span></span>

```qsharp
ApplyToEachCA(H, register);
```

<span data-ttu-id="b6381-118">Hier geeft het achtervoegsel `CA` aan dat de aanroep naar `ApplyToEach` zichzelf adjointable en kan worden aangeraden.</span><span class="sxs-lookup"><span data-stu-id="b6381-118">Here, the suffix `CA` indicates that the call to `ApplyToEach` is itself adjointable and controllable.</span></span>
<span data-ttu-id="b6381-119">Als `U` dit wel het geval is, `Adjoint` `Controlled` zijn de volgende regels gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="b6381-119">Thus, if `U` supports `Adjoint` and `Controlled`, the following lines are equivalent:</span></span>

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

<span data-ttu-id="b6381-120">Dit betekent met name dat aanroepen naar `ApplyToEachCA` kunnen worden weer gegeven in bewerkingen waarvoor een adjoint-specialisatie automatisch wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b6381-120">In particular, this means that calls to `ApplyToEachCA` can appear in operations for which an adjoint specialization is auto-generated.</span></span>
<span data-ttu-id="b6381-121"><xref:microsoft.quantum.canon.applytoeachindex>Het is ook nuttig om patronen van het formulier weer `U(0, targets[0]); U(1, targets[1]); ...` te geven en biedt versies voor elke combi natie van functors die wordt ondersteund door de invoer.</span><span class="sxs-lookup"><span data-stu-id="b6381-121">Similarly, <xref:microsoft.quantum.canon.applytoeachindex> is useful for representing patterns of the form `U(0, targets[0]); U(1, targets[1]); ...`, and offers versions for each combination of functors supported by its input.</span></span>

> [!TIP]
> <span data-ttu-id="b6381-122">`ApplyToEach` is type-para meters, zodat deze kan worden gebruikt met bewerkingen die andere invoer hebben dan `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="b6381-122">`ApplyToEach` is type-parameterized such that it can be used with operations that take inputs other than `Qubit`.</span></span>
> <span data-ttu-id="b6381-123">Stel bijvoorbeeld dat `codeBlocks` een matrix met <xref:microsoft.quantum.errorcorrection.logicalregister> waarden is die moeten worden hersteld.</span><span class="sxs-lookup"><span data-stu-id="b6381-123">For example, suppose that `codeBlocks` is an array of <xref:microsoft.quantum.errorcorrection.logicalregister> values that need to be recovered.</span></span>
> <span data-ttu-id="b6381-124">Vervolgens `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` worden de fout correctie code `code` en de herstel functie `recoveryFn` op elk afzonderlijk blok toegepast.</span><span class="sxs-lookup"><span data-stu-id="b6381-124">Then `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` will apply the error-correcting code `code` and recovery function `recoveryFn` to each block independently.</span></span>
> <span data-ttu-id="b6381-125">Dit geldt ook voor klassieke invoer: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` past een rotatie toe van $ \pi/$2 over $X $, gevolgd door een rotatie van $Pi/$3 over $Y $.</span><span class="sxs-lookup"><span data-stu-id="b6381-125">This holds even for classical inputs: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` will apply a rotation of $\pi / 2$ about $X$ followed by a rotation of $pi / 3$ about $Y$.</span></span>

<span data-ttu-id="b6381-126">De Q# Canon biedt ook ondersteuning voor klassieke inventarisatie patronen die bekend zijn met functionele programmering.</span><span class="sxs-lookup"><span data-stu-id="b6381-126">The Q# canon also provides support for classical enumeration patterns familiar to functional programming.</span></span>
<span data-ttu-id="b6381-127">Bijvoorbeeld: <xref:microsoft.quantum.arrays.fold> implementeert het patroon $f (f (f (s \_ {\Text{Initial}}, x \_ 0), x \_ 1), \dots) $ voor het verkleinen van een functie over een lijst.</span><span class="sxs-lookup"><span data-stu-id="b6381-127">For instance, <xref:microsoft.quantum.arrays.fold> implements the pattern $f(f(f(s\_{\text{initial}}, x\_0), x\_1), \dots)$ for reducing a function over a list.</span></span>
<span data-ttu-id="b6381-128">Dit patroon kan worden gebruikt voor het implementeren van sommen, producten, minima, maxima en andere dergelijke functies:</span><span class="sxs-lookup"><span data-stu-id="b6381-128">This pattern can be used to implement sums, products, minima, maxima and other such functions:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

<span data-ttu-id="b6381-129">Op dezelfde manier werken functies zoals <xref:microsoft.quantum.arrays.mapped> en <xref:microsoft.quantum.arrays.mappedbyindex> kunnen worden gebruikt voor het uitdrukken van functionele Programmeer concepten in Q# .</span><span class="sxs-lookup"><span data-stu-id="b6381-129">Similarly, functions like <xref:microsoft.quantum.arrays.mapped> and <xref:microsoft.quantum.arrays.mappedbyindex> can be used to express functional programming concepts in Q#.</span></span>

## <a name="composing-operations-and-functions"></a><span data-ttu-id="b6381-130">Bewerkingen en functies samen stellen</span><span class="sxs-lookup"><span data-stu-id="b6381-130">Composing Operations and Functions</span></span> ##

<span data-ttu-id="b6381-131">De constructies van de besturings stroom die door de Canon worden aangeboden, nemen activiteiten en functies als invoer, zodat het handig is om verschillende bewerkingen of functies in te stellen in één aanroepable.</span><span class="sxs-lookup"><span data-stu-id="b6381-131">The control flow constructs offered by the canon take operations and functions as their inputs, such that it is helpful to be able to compose several operations or functions into a single callable.</span></span>
<span data-ttu-id="b6381-132">Het patroon $UVU ^ {\dagger} $ is bijvoorbeeld zeer gebruikelijk in Quantum Program ma's, zodat de Canon de bewerking <xref:microsoft.quantum.canon.applywith> als een abstractie van dit patroon biedt.</span><span class="sxs-lookup"><span data-stu-id="b6381-132">For instance, the pattern $UVU^{\dagger}$ is extremely common in quantum programming, such that the canon provides the operation <xref:microsoft.quantum.canon.applywith> as an abstraction for this pattern.</span></span>
<span data-ttu-id="b6381-133">Deze abstractie biedt ook een efficiëntere naleving van circuits, zoals het uitvoeren `Controlled` van de reeks `U(qubit); V(qubit); Adjoint U(qubit);` hoeft niet op elke handeling te reageren `U` .</span><span class="sxs-lookup"><span data-stu-id="b6381-133">This abstraction also allows for more efficient compliation into circuits, as `Controlled` acting on the sequence `U(qubit); V(qubit); Adjoint U(qubit);` does not need to act on each `U`.</span></span>
<span data-ttu-id="b6381-134">Als u dit wilt zien, laat u $c (U) $ de unitary vertegenwoordigen `Controlled U([control], target)` en laat $c (V) $ op dezelfde manier worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b6381-134">To see this, let $c(U)$ be the unitary representing `Controlled U([control], target)` and let $c(V)$ be defined in the same way.</span></span>
<span data-ttu-id="b6381-135">Klik vervolgens voor een wille keurige status $ \ket{\psi} $, \begin{align} c (U) c (V) c (U) ^ \dagger \ket {1} \otimes \ket{\psi} & = \ket {1} \OTIMES (UVU ^ {\dagger} \ket{\psi}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {1} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="b6381-135">Then for an arbitrary state $\ket{\psi}$, \begin{align} c(U) c(V) c(U)^\dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU^{\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{1} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="b6381-136">\end{align} op basis van de definitie van `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="b6381-136">\end{align} by the definition of `Controlled`.</span></span>
<span data-ttu-id="b6381-137">Anderzijds \begin{align} c (U) c (V) c (U) ^ \dagger \ket {0} \otimes \ket{\psi} & = \ket {0} \otimes \ket{\psi} \\ \\ & = \ket {0} \otimes (UU ^ \dagger \ket{\psi}) \\ \\ & = (\Boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {0} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="b6381-137">On the other hand, \begin{align} c(U) c(V) c(U)^\dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU^\dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{0} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="b6381-138">\end{align} op basis van lineariteit kunnen we concluderen dat $U $ op deze manier kan worden gefactord voor alle invoer Staten.</span><span class="sxs-lookup"><span data-stu-id="b6381-138">\end{align} By linearity, we can conclude that we can factor $U$ out in this way for all input states.</span></span>
<span data-ttu-id="b6381-139">Dat wil zeggen, $c (UVU ^ \dagger) = U c (V) U ^ \dagger $.</span><span class="sxs-lookup"><span data-stu-id="b6381-139">That is, $c(UVU^\dagger) = U c(V) U^\dagger$.</span></span>
<span data-ttu-id="b6381-140">Omdat het beheren van bewerkingen duur in het algemeen is, `WithC` `WithCA` kunt u het aantal controle-functors dat moet worden toegepast, beperken met behulp van beheerde varianten, zoals en.</span><span class="sxs-lookup"><span data-stu-id="b6381-140">Since controlling operations can be expensive in general, using controlled variants such as `WithC` and `WithCA` can help reduce the number of control functors that need to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="b6381-141">Een andere consequentie van het factor maken van $U $ is dat we niet eens weten hoe de `Controlled` functor moet worden toegepast `U` .</span><span class="sxs-lookup"><span data-stu-id="b6381-141">One other consequence of factoring out $U$ is that we need not even know how to apply the `Controlled` functor to `U`.</span></span>
> <span data-ttu-id="b6381-142">`ApplyWithCA` heeft daarom een zwakkere hand tekening dan verwacht:</span><span class="sxs-lookup"><span data-stu-id="b6381-142">`ApplyWithCA` therefore has a weaker signature than might be expected:</span></span>
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

<span data-ttu-id="b6381-143">Op dezelfde manier worden <xref:microsoft.quantum.canon.bound> er bewerkingen uitgevoerd waarbij een reeks andere bewerkingen op zijn beurt wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="b6381-143">Similarly, <xref:microsoft.quantum.canon.bound> produces operations which apply a sequence of other operations in turn.</span></span>
<span data-ttu-id="b6381-144">Het volgende is bijvoorbeeld gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="b6381-144">For instance, the following are equivalent:</span></span>

```qsharp
H(qubit); X(qubit);
Bound([H, X], qubit);
```

<span data-ttu-id="b6381-145">Combi neren met iteratie patronen kan dit met name nuttig maken:</span><span class="sxs-lookup"><span data-stu-id="b6381-145">Combining with iteration patterns can make this especially useful:</span></span>

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bound([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a><span data-ttu-id="b6381-146">Samen stelling met time-bestelling</span><span class="sxs-lookup"><span data-stu-id="b6381-146">Time-Ordered Composition</span></span> ###

<span data-ttu-id="b6381-147">We kunnen nog steeds verder gaan met de Datatransport besturing in termen van gedeeltelijke toepassing en klassieke functies, en kunnen zelfs redelijk geraffineerde Quantum concepten model leren in termen van klassiek stroom beheer.</span><span class="sxs-lookup"><span data-stu-id="b6381-147">We can go still further by thinking of flow control in terms of partial application and classical functions, and can model even fairly sophisticated quantum concepts in terms of classical flow control.</span></span>
<span data-ttu-id="b6381-148">Deze analoge bepaling wordt nauw keurig gemaakt door de erkenning dat unitary-Opera tors precies overeenkomen met de neven effecten van aanroepende activiteiten, zodat een degelijkheid van unitary-Opera tors in termen van andere unitary-Opera tors overeenkomt met het bouwen van een bepaalde aanroep volgorde voor klassieke subroutines die instructies verzenden om te fungeren als bepaalde unitary-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="b6381-148">This analogy is made precise by the recognition that unitary operators correspond exactly to the side effects of calling operations, such that any decomposition of unitary operators in terms of other unitary operators corresponds to constructing a particular calling sequence for classical subroutines which emit instructions to act as particular unitary operators.</span></span>
<span data-ttu-id="b6381-149">In deze weer gave `Bound` is de representatie van het matrix product nauw keurig, omdat dit `Bound([A, B])(target)` gelijk is aan `A(target); B(target);` , die op zijn beurt de aanroep volgorde is die overeenkomt met $BA $.</span><span class="sxs-lookup"><span data-stu-id="b6381-149">Under this view, `Bound` is precisely the representation of the matrix product, since `Bound([A, B])(target)` is equivalent to `A(target); B(target);`, which in turn is the calling sequence corresponding to $BA$.</span></span>

<span data-ttu-id="b6381-150">Een geavanceerd voor beeld is de [Trotter – Suzuki-uitbrei ding](https://arxiv.org/abs/math-ph/0506007v1).</span><span class="sxs-lookup"><span data-stu-id="b6381-150">A more sophisticated example is the [Trotter–Suzuki expansion](https://arxiv.org/abs/math-ph/0506007v1).</span></span>
<span data-ttu-id="b6381-151">Zoals beschreven in de sectie voor het weer geven van dynamische Generator van [gegevens structuren](xref:microsoft.quantum.libraries.data-structures), biedt de Trotter-Suzuki-uitbrei ding een bijzonder nuttige manier om matrix-exponentiëlen uit te geven.</span><span class="sxs-lookup"><span data-stu-id="b6381-151">As discussed in the Dynamical Generator Representation section of [data structures](xref:microsoft.quantum.libraries.data-structures), the Trotter–Suzuki expansion provides a particularly useful way of expressing matrix exponentials.</span></span>
<span data-ttu-id="b6381-152">Bijvoorbeeld: het Toep assen van de uitbrei ding met het laagste Volg nummer dat voor Opera tors $A $ en $B $ zodanig is dat $A = A ^ \dagger $ en $B = B ^ \dagger $, \begin{align} \tag{★} \label{EQ: Trotter-Suzuki-0} \exp (i [A + B] t) = \ lim_ {n\to\infty} \left (\exp (i A t/n) \exp (i B t/n) \right) ^ n.</span><span class="sxs-lookup"><span data-stu-id="b6381-152">For instance, applying the expansion at its lowest order yields that for any operators $A$ and $B$ such that $A = A^\dagger$ and $B = B^\dagger$, \begin{align} \tag{★} \label{eq:trotter-suzuki-0} \exp(i [A + B] t) = \lim_{n\to\infty} \left(\exp(i A t / n) \exp(i B t / n)\right)^n.</span></span>
<span data-ttu-id="b6381-153">\end{align} Colloquially, dit geeft aan dat we ongeveer een staat kunnen ontwikkelen onder $A + B $ door zich op een andere wijze te ontwikkelen onder $A $ en $B $ alleen.</span><span class="sxs-lookup"><span data-stu-id="b6381-153">\end{align} Colloquially, this says that we can approximately evolve a state under $A + B$ by alternately evolving under $A$ and $B$ alone.</span></span>
<span data-ttu-id="b6381-154">Als we de ontwikkeling onder $A $ vertegenwoordigen door een bewerking `A : (Double, Qubit[]) => Unit` die van toepassing is op $e ^ {i t A} $, wordt de representatie van de Trotter-Suzuki-uitbrei ding voor het opnieuw ordenen van oproep reeksen duidelijk.</span><span class="sxs-lookup"><span data-stu-id="b6381-154">If we represent evolution under $A$ by an operation `A : (Double, Qubit[]) => Unit` that applies $e^{i t A}$, then the representation of the Trotter–Suzuki expansion in terms of rearranging calling sequences becomes clear.</span></span>
<span data-ttu-id="b6381-155">Gezien een bewerking `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` zoals `A = U(0, _, _)` en `B = U(1, _, _)` , kunnen we een nieuwe bewerking definiëren voor de integraal van `U` op tijdstip $t $ door het genereren van reeksen van het formulier</span><span class="sxs-lookup"><span data-stu-id="b6381-155">Concretely, given an operation `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` such that `A = U(0, _, _)` and `B = U(1, _, _)`, we can define a new operation representing the integral of `U` at time $t$ by generating sequences of the form</span></span>

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

<span data-ttu-id="b6381-156">Op dit moment kunnen we nu de oorzaak van de Trotter – Suzuki-uitbrei ding *zonder verwijzing naar Quantum monteurs*.</span><span class="sxs-lookup"><span data-stu-id="b6381-156">At this point, we can now reason about the Trotter–Suzuki expansion *without reference to quantum mechanics at all*.</span></span>
<span data-ttu-id="b6381-157">De uitbrei ding is in feite een zeer specifiek herhalings patroon dat wordt gemotiveerd door $ \eqref{EQ: Trotter-Suzuki-0} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-157">The expansion is effectively a very particular iteration pattern motivated by $\eqref{eq:trotter-suzuki-0}$.</span></span>
<span data-ttu-id="b6381-158">Dit herhalings patroon wordt geïmplementeerd door <xref:microsoft.quantum.canon.decomposeintotimestepsca> :</span><span class="sxs-lookup"><span data-stu-id="b6381-158">This iteration pattern is implemented by <xref:microsoft.quantum.canon.decomposeintotimestepsca>:</span></span>

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

<span data-ttu-id="b6381-159">De hand tekening van `DecomposeIntoTimeStepsCA` volgt een gemeen schappelijk patroon in Q# , waarbij verzamelingen waarvan een back-up kan worden gemaakt, worden weer gegeven door middel van matrices of door een van de elementen die in de vlucht worden berekend door tupels waarvan de eerste elementen `Int` waarden aangeven die de lengte van die gegevens.</span><span class="sxs-lookup"><span data-stu-id="b6381-159">The signature of `DecomposeIntoTimeStepsCA` follows a common pattern in Q#, where collections that may be backed either by arrays or by something which compute elements on the fly are represented by tuples whose first elements are `Int` values indicating their lengths.</span></span>

## <a name="putting-it-together-controlling-operations"></a><span data-ttu-id="b6381-160">Samen te brengen: bewerkingen beheren</span><span class="sxs-lookup"><span data-stu-id="b6381-160">Putting it Together: Controlling Operations</span></span> ##

<span data-ttu-id="b6381-161">Ten slotte bouwt de Canon op het `Controlled` functor door extra manieren te bieden voor het afwegen van Quantum bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="b6381-161">Finally, the canon builds on the `Controlled` functor by providing additional ways to condition quantum operations.</span></span>
<span data-ttu-id="b6381-162">Het is gebruikelijk, met name bij Quantum wiskundige bewerkingen, tot voor waarden voor de berekening van andere berekenings statussen dan $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-162">It is common, especially in quantum arithmetic, to condition operations on computational basis states other than $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="b6381-163">Met behulp van de besturings elementen en functies die hierboven worden geïntroduceerd, kunnen we meer algemene Quantum voorwaarden in één instructie hebben.</span><span class="sxs-lookup"><span data-stu-id="b6381-163">Using the control operations and functions introduced above, we can more general quantum conditions in a single statement.</span></span>
<span data-ttu-id="b6381-164">We gaan naar hoe <xref:microsoft.quantum.canon.controlledonbitstring> werkt het (type para meters voor san's), waarna de onderdelen één voor één worden opgesplitst.</span><span class="sxs-lookup"><span data-stu-id="b6381-164">Let's jump in to how <xref:microsoft.quantum.canon.controlledonbitstring> does it (sans type parameters), then we'll break down the pieces one by one.</span></span>
<span data-ttu-id="b6381-165">Het eerste wat u moet doen, is het definiëren van een bewerking die werkelijk het zware werk van het beheer op basis van een wille keurige reken status heeft.</span><span class="sxs-lookup"><span data-stu-id="b6381-165">The first thing we'll need to do is to define an operation which actually does the heavy lifting of implementing the control on arbitrary computational basis states.</span></span>
<span data-ttu-id="b6381-166">Deze bewerking wordt echter niet rechtstreeks aangeroepen, maar daarom voegen we toe `_` aan het begin van de naam om aan te geven dat het een implementatie van een andere construct elders is.</span><span class="sxs-lookup"><span data-stu-id="b6381-166">We won't call this operation directly, however, and so we add `_` to the beginning of the name to indicate that it's an implementation of another construct elsewhere.</span></span>

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

<span data-ttu-id="b6381-167">Houd er rekening mee dat we een reeks bits gebruiken die wordt weer gegeven als een `Bool` matrix. deze worden gebruikt om de voor waarden op te geven die u wilt Toep assen op de bewerking `oracle` die we hebben opgegeven.</span><span class="sxs-lookup"><span data-stu-id="b6381-167">Note that we take a string of bits, represented as a `Bool` array, that we use to specify the conditioning that we want to apply to the operation `oracle` that we are given.</span></span>
<span data-ttu-id="b6381-168">Aangezien deze bewerking rechtstreeks de toepassing doet, moeten we ook het besturings element en de doel registers volgen, die hier worden weer gegeven als `Qubit[]` .</span><span class="sxs-lookup"><span data-stu-id="b6381-168">Since this operation actually does the application directly, we also need to take the control and target registers, both represented here as `Qubit[]`.</span></span>

<span data-ttu-id="b6381-169">Vervolgens zien we dat er wordt gewaakt over de status van berekening op basis van \ket{\vec{s}} = \ket{s \_ 0 s \_ 1 \dots s \_ {n-1}} $ voor een bits-teken reeks $ \vec{s} $ kan worden gerealiseerd door $ \ket{\vec{s}} $ te transformeren naar $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-169">Next, we note that controlling on the computational basis state $\ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n - 1}}$ for a bit string $\vec{s}$ can be realized by transforming $\ket{\vec{s}}$ into $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="b6381-170">Met name $ \ket{\vec{s}} = X ^ {s \_ 0} \Otimes X ^ {s \_ 1} \otimes \Cdots \otimes X ^ {s \_ {n-1}} \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-170">In particular, $\ket{\vec{s}} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{0\cdots 0}$.</span></span>
<span data-ttu-id="b6381-171">Sinds $X ^ {\dagger} = X $, betekent dit dat $ \ket{0\dots 0} = X ^ {s \_ 0} \Otimes X ^ {s \_ 1} \otimes \Cdots \otimes X ^ {s \_ {n-1}} \ket{\vec{s}} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-171">Since $X^{\dagger} = X$, this implies that $\ket{0\dots 0} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{\vec{s}}$.</span></span>
<span data-ttu-id="b6381-172">Daarom kunnen we $P Toep assen = X ^ {s \_ 0} \Otimes x ^ {s \_ 1} \otimes \Cdots \otimes x ^ {s \_ {n-1}} $, apply en `Controlled oracle` retransform to $ \vec{s} $.</span><span class="sxs-lookup"><span data-stu-id="b6381-172">Thus, we can apply $P = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}}$, apply `Controlled oracle`, and transform back to $\vec{s}$.</span></span>
<span data-ttu-id="b6381-173">Deze constructie is nauw keurig `ApplyWith` , dus we schrijven de hoofd tekst van de nieuwe bewerking dienovereenkomstig:</span><span class="sxs-lookup"><span data-stu-id="b6381-173">This construction is precisely `ApplyWith`, so we write the body of our new operation accordingly:</span></span>

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

<span data-ttu-id="b6381-174">Hier zijn we gebruikt <xref:microsoft.quantum.canon.applypaulifrombitstring> om $P $ toe te passen, die gedeeltelijk van toepassing zijn op het doel voor gebruik met `ApplyWith` .</span><span class="sxs-lookup"><span data-stu-id="b6381-174">Here, we have used <xref:microsoft.quantum.canon.applypaulifrombitstring> to apply $P$, partially applying over its target for use with `ApplyWith`.</span></span>
<span data-ttu-id="b6381-175">Houd er echter rekening mee dat het *controle* register moet worden getransformeerd naar het gewenste formulier, dus we passen de binnenste bewerking `(Controlled oracle)` op het *doel*gedeeltelijk toe.</span><span class="sxs-lookup"><span data-stu-id="b6381-175">Note, however, that we need to transform the *control* register to our desired form, so we partially apply the inner operation `(Controlled oracle)` on the *target*.</span></span>
<span data-ttu-id="b6381-176">Dit `ApplyWith` houdt in dat u het controle register met $P $ kunt sluiten, precies zoals gewenst.</span><span class="sxs-lookup"><span data-stu-id="b6381-176">This leaves `ApplyWith` acting to bracket the control register with $P$, exactly as we desired.</span></span>

<span data-ttu-id="b6381-177">Op dit moment kunnen we worden uitgevoerd, maar het lijkt erop dat onze nieuwe bewerking niet lijkt, zoals het Toep assen van de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="b6381-177">At this point, we could be done, but it is somehow unsatisfying that our new operation does not "feel" like applying the `Controlled` functor.</span></span>
<span data-ttu-id="b6381-178">Daarom volt ooien we het nieuwe controle stroom concept door een functie te schrijven waarmee de Oracle wordt gecontroleerd en een nieuwe bewerking wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="b6381-178">Thus, we finish defining our new control flow concept by writing a function that takes the oracle to be controlled and that returns a new operation.</span></span>
<span data-ttu-id="b6381-179">Op deze manier ziet onze nieuwe functie er ongeveer als volgt uit, wat erop `Controlled` kan zien dat we eenvoudig krachtige nieuwe constructies voor de controle stroom kunnen definiëren met Q# en de Canon:</span><span class="sxs-lookup"><span data-stu-id="b6381-179">In this way, our new function looks and feels very much like `Controlled`, illustrating that we can easily define powerful new control flow constructs using Q# and the canon together:</span></span>

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
