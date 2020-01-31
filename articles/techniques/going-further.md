---
title: 'Verdere Q # technieken | Microsoft Docs'
description: 'Verdere Q # technieken'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.going-further
ms.openlocfilehash: bd2b799d4001e280baccb04158247891b9cbb5bc
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820195"
---
# <a name="going-further"></a><span data-ttu-id="fd747-103">Verder gaan</span><span class="sxs-lookup"><span data-stu-id="fd747-103">Going Further</span></span> #

<span data-ttu-id="fd747-104">Nu u hebt gezien hoe u interessante Quantum Programma's schrijft in Q #, gaat u naar deze sectie voor meer informatie over een aantal geavanceerde onderwerpen die nuttig moeten worden behandeld.</span><span class="sxs-lookup"><span data-stu-id="fd747-104">Now that you've seen how to write interesting quantum programs in Q#, this section goes further by introducing a few more advanced topics that should prove useful going forward.</span></span>


## <a name="generic-operations-and-functions"></a><span data-ttu-id="fd747-105">Algemene bewerkingen en functies</span><span class="sxs-lookup"><span data-stu-id="fd747-105">Generic Operations and Functions</span></span> ##

> [!TIP]
> <span data-ttu-id="fd747-106">In deze sectie wordt ervan uitgegaan dat u bekend bent met [algemene C# ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics)kennis in, [generieke F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [ C++ sjablonen](https://docs.microsoft.com/cpp/cpp/templates-cpp)of soort gelijke benaderingen voor het Program meren in andere talen.</span><span class="sxs-lookup"><span data-stu-id="fd747-106">This section assumes some basic familiarity with [generics in C#](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [generics in F#](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [C++ templates](https://docs.microsoft.com/cpp/cpp/templates-cpp), or similar approaches to metaprogramming in other languages.</span></span>

<span data-ttu-id="fd747-107">Veel functies en bewerkingen die u mogelijk wilt definiëren, zijn niet echt afhankelijk van de typen invoer, maar u kunt de typen echter alleen impliciet gebruiken via een andere functie of bewerking.</span><span class="sxs-lookup"><span data-stu-id="fd747-107">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="fd747-108">Stel dat het *kaart* concept gebruikelijk is in veel functionele talen. met een functie $f (x) $ en een verzameling waarden $\{x_1, x_2, \dots, x_n\}$, kaart retourneert een nieuwe verzameling $\{f (x_1), f (x_2), \dots, f (x_n)\}$.</span><span class="sxs-lookup"><span data-stu-id="fd747-108">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="fd747-109">Om dit in Q # te implementeren, kunnen we profiteren van die functies de eerste klasse.</span><span class="sxs-lookup"><span data-stu-id="fd747-109">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="fd747-110">We gaan een snel voor beeld van `Map`schrijven, met behulp van ★ als tijdelijke aanduiding, terwijl we weten welke typen we nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="fd747-110">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : ★ -> ★, values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fd747-111">Houd er rekening mee dat deze functie veel hetzelfde lijkt, ongeacht de werkelijke typen die we vervangen.</span><span class="sxs-lookup"><span data-stu-id="fd747-111">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="fd747-112">Een kaart van gehele getallen tot Paulis, bijvoorbeeld ziet er ongeveer hetzelfde uit als een kaart van drijvende-komma getallen naar teken reeksen:</span><span class="sxs-lookup"><span data-stu-id="fd747-112">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : Int -> Pauli, values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : Double -> String, values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fd747-113">In principe kunnen we een versie van `Map` schrijven voor elk paar typen dat we tegen komen, maar dit heeft een aantal problemen.</span><span class="sxs-lookup"><span data-stu-id="fd747-113">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="fd747-114">Als we bijvoorbeeld een bug in `Map`vinden, moeten we ervoor zorgen dat de oplossing op uniforme wijze wordt toegepast in alle versies van `Map`.</span><span class="sxs-lookup"><span data-stu-id="fd747-114">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="fd747-115">Als we een nieuwe tuple of UDT bouwen, moeten we nu ook een nieuwe `Map` maken om samen met het nieuwe type te gaan.</span><span class="sxs-lookup"><span data-stu-id="fd747-115">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="fd747-116">Hoewel dit kan worden ondervangen voor een klein aantal dergelijke functies, omdat we meer en meer functies van hetzelfde formulier verzamelen als `Map`, zijn de kosten van het introduceren van nieuwe typen onredelijk groot in redelijk korte volg orde.</span><span class="sxs-lookup"><span data-stu-id="fd747-116">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="fd747-117">Veel van deze problemen kunnen er echter toe leiden dat de informatie die nodig is om te bepalen hoe de verschillende versies van `Map` zijn gerelateerd, niet aan de compiler is gegeven.</span><span class="sxs-lookup"><span data-stu-id="fd747-117">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="fd747-118">We willen het compileren om `Map` te behandelen als een soort wiskundige functie van Q #- *typen* tot q #-functies.</span><span class="sxs-lookup"><span data-stu-id="fd747-118">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>
<span data-ttu-id="fd747-119">Dit principe wordt formeel door het toestaan van functies en bewerkingen om *type parameters*te hebben, evenals de normale tuple-para meters.</span><span class="sxs-lookup"><span data-stu-id="fd747-119">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="fd747-120">In de bovenstaande voor beelden willen we `Map` zien als having-para meters `Int, Pauli` in het eerste geval en `Double, String` in het tweede geval.</span><span class="sxs-lookup"><span data-stu-id="fd747-120">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="fd747-121">In het algemeen kunnen deze type parameters vervolgens worden gebruikt alsof het normale typen zijn: we gebruiken waarden van het type para meters om matrices en Tuples te maken, functies en bewerkingen aan te roepen en toe te wijzen aan gewone of onveranderlijke variabelen.</span><span class="sxs-lookup"><span data-stu-id="fd747-121">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="fd747-122">Het meest extreme geval van indirecte afhankelijkheid is die van qubits, waarbij een Q #-programma niet rechtstreeks kan vertrouwen op de structuur van het `Qubit` type, maar **moet** dergelijke typen door geven aan andere bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="fd747-122">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="fd747-123">Als u terugkeert naar bovenstaand voor beeld, kunnen we zien dat `Map` over de type parameters moet beschikken, een voor de invoer van `fn` en één om de uitvoer van `fn`weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fd747-123">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="fd747-124">In Q # wordt dit geschreven door punt haken toe te voegen (dat is `<>`, niet brakets $ \braket{}$!) na de naam van een functie of bewerking in de declaratie ervan en door elk type para meter te vermelden.</span><span class="sxs-lookup"><span data-stu-id="fd747-124">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="fd747-125">De naam van elke type parameter moet beginnen met een Tick `'`, wat aangeeft dat het een type parameter is en niet een gewoon type (ook wel een *concreet* type genoemd).</span><span class="sxs-lookup"><span data-stu-id="fd747-125">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="fd747-126">Voor `Map`kunnen we het volgende schrijven:</span><span class="sxs-lookup"><span data-stu-id="fd747-126">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : 'Input -> 'Output, values : 'Input[]) : 'Output {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fd747-127">Houd er rekening mee dat de definitie van `Map<'Input, 'Output>` erg lijkt op de versies die we eerder hebben afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="fd747-127">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="fd747-128">Het enige verschil is dat we de compiler expliciet hebben geïnformeerd dat `Map` niet rechtstreeks afhankelijk is van wat `'Input` en `'Output` zijn, maar voor elk van beide typen indirect via `fn`.</span><span class="sxs-lookup"><span data-stu-id="fd747-128">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="fd747-129">Zodra we `Map<'Input, 'Output>` op deze manier hebben gedefinieerd, kunnen we deze aanroepen alsof het een gewone functie was:</span><span class="sxs-lookup"><span data-stu-id="fd747-129">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="fd747-130">Het schrijven van algemene functies en bewerkingen is een plek waar ' tuple-in ' tuple-out ' een zeer handige manier is om te denken over Q #-functies en-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="fd747-130">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="fd747-131">Omdat elke functie precies één invoer heeft en er precies één uitvoer wordt geretourneerd, wordt een invoer van het type `'T -> 'U` overeenkomt met *een* Q #-functie.</span><span class="sxs-lookup"><span data-stu-id="fd747-131">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="fd747-132">Op dezelfde manier kan elke bewerking worden door gegeven aan een invoer van het type `'T => 'U`.</span><span class="sxs-lookup"><span data-stu-id="fd747-132">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="fd747-133">Als tweede voor beeld moet u de uitdaging van het schrijven van een functie die de samen stelling van twee andere functies retourneert, overwegen:</span><span class="sxs-lookup"><span data-stu-id="fd747-133">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="fd747-134">Hier moeten we precies opgeven wat `A`, `B`en `C` zijn, waardoor het hulp programma van onze nieuwe `Compose` functie aanzienlijk wordt beperkt.</span><span class="sxs-lookup"><span data-stu-id="fd747-134">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="fd747-135">Na alle is `Compose` alleen afhankelijk van `A`, `B`en `C` *via* `innerFn` en `outerFn`.</span><span class="sxs-lookup"><span data-stu-id="fd747-135">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="fd747-136">Als alternatief kunnen we type parameters toevoegen aan `Compose` die aangeven dat het werkt voor *alle* `A`, `B`en `C`, zolang deze para meters overeenkomen met de verwachte `innerFn` en `outerFn`:</span><span class="sxs-lookup"><span data-stu-id="fd747-136">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="fd747-137">De standaard bibliotheken van Q # bieden een reeks dergelijke bewerkingen en functies van type para meters waarmee de controle stroom van een hogere volg orde eenvoudiger kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd747-137">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="fd747-138">Deze worden verder besproken in de [hand leiding Q # Standard Library](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="fd747-138">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="borrowing-qubits"></a><span data-ttu-id="fd747-139">Lenende qubits</span><span class="sxs-lookup"><span data-stu-id="fd747-139">Borrowing Qubits</span></span> ##

<span data-ttu-id="fd747-140">Met het lenende mechanisme kunt u de toewijzing van qubits die als Scratch ruimte kan worden gebruikt tijdens een berekening.</span><span class="sxs-lookup"><span data-stu-id="fd747-140">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span> <span data-ttu-id="fd747-141">Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="fd747-141">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span> <span data-ttu-id="fd747-142">Een van de ' Dirty ' qubits als hun status is onbekend en kan zelfs worden Entangled met andere delen van het geheugen van de quantum computer.</span><span class="sxs-lookup"><span data-stu-id="fd747-142">One also speaks of "dirty" qubits as their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span> <span data-ttu-id="fd747-143">In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.</span><span class="sxs-lookup"><span data-stu-id="fd747-143">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>

<span data-ttu-id="fd747-144">In de Canon zijn voor beelden die gebruikmaken van het sleutel woord `borrowing`, bijvoorbeeld de functie `MultiControlledXBorrow` hieronder gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="fd747-144">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="fd747-145">Als `controls` het besturings element qubits dat moet worden toegevoegd aan een `X` bewerking, wordt er in het algemeen `Length(controls)-2` veel vuil ancillas toegevoegd door deze implementatie.</span><span class="sxs-lookup"><span data-stu-id="fd747-145">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="fd747-146">Houd er rekening mee dat uitgebreid gebruik van de `With` Combinator---in het formulier dat van toepassing is op bewerkingen die ondersteuning bieden voor adjoint, dat wil zeggen `WithA`---is gemaakt in dit voor beeld. Dit is een goede programmeer stijl als het toevoegen van besturings elementen aan structuren die `With` alleen besturings elementen door geven aan de binnenste bewerking.</span><span class="sxs-lookup"><span data-stu-id="fd747-146">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example which is good programming style as adding control to structures involving `With` only propagates control to the inner operation.</span></span> <span data-ttu-id="fd747-147">Naast de `body` van de bewerking is een implementatie van de `controlled` hoofd tekst van de bewerking expliciet gegeven, in plaats van een `controlled auto`-instructie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fd747-147">Further note that here in addition to the `body` of the operation an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span> <span data-ttu-id="fd747-148">De reden hiervoor is dat we van de structuur van het circuit weten hoe u gemakkelijk verdere controles kunt toevoegen die nuttig zijn voor het toevoegen van controle aan elke afzonderlijke poort in de `body`.</span><span class="sxs-lookup"><span data-stu-id="fd747-148">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="fd747-149">Het is een goed proces om deze code te vergelijken met een andere Canon-functie `MultiControlledXClean` die hetzelfde doel heeft als het implementeren van een met vermenigvuldiging beheerde `X`-bewerking, die gebruikmaakt van verschillende schone qubits met behulp van het `using`-mechanisme.</span><span class="sxs-lookup"><span data-stu-id="fd747-149">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 
