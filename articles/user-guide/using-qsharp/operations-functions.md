---
title: 'Bewerkingen en functies in Q #'
description: Bewerkingen en functies definiëren en aanroepen, evenals de gecontroleerde en adjoint bewerkingen.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: 6cfc1b14d86e86a1cbf0109d5e81dfe50c3a80bf
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630218"
---
# <a name="operations-and-functions-in-q"></a><span data-ttu-id="992be-103">Bewerkingen en functies in Q #</span><span class="sxs-lookup"><span data-stu-id="992be-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="992be-104">Nieuwe bewerkingen definiëren</span><span class="sxs-lookup"><span data-stu-id="992be-104">Defining New Operations</span></span>

<span data-ttu-id="992be-105">Bewerkingen zijn de kern van Q #.</span><span class="sxs-lookup"><span data-stu-id="992be-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="992be-106">Als ze zijn gedeclareerd, kunnen ze worden aangeroepen vanuit klassieke .NET-toepassingen, bijvoorbeeld met behulp van een Simulator of door andere bewerkingen binnen Q #.</span><span class="sxs-lookup"><span data-stu-id="992be-106">Once declared, they can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="992be-107">Elke bewerking die is gedefinieerd in Q # kan vervolgens een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde intrinsieke bewerkingen die zijn gedefinieerd door de taal.</span><span class="sxs-lookup"><span data-stu-id="992be-107">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="992be-108">De specifieke manier waarop deze intrinsieke bewerkingen worden gedefinieerd, is afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="992be-108">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span>
<span data-ttu-id="992be-109">Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.</span><span class="sxs-lookup"><span data-stu-id="992be-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="992be-110">Elk Q #-bron bestand kan een wille keurig aantal bewerkingen definiëren.</span><span class="sxs-lookup"><span data-stu-id="992be-110">Each Q# source file may define any number of operations.</span></span>
<span data-ttu-id="992be-111">Bewerkings namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met type-of functie namen.</span><span class="sxs-lookup"><span data-stu-id="992be-111">Operation names must be unique within a namespace and may not conflict with type or function names.</span></span>

<span data-ttu-id="992be-112">Een bewerkings declaratie bestaat uit het tref woord `operation` , gevolgd door het symbool dat de naam van de bewerking is, een getypeerde id-tupel waarmee de argumenten voor de bewerking worden gedefinieerd, een dubbele punt `:` , een type aantekening waarmee het resultaat type van de bewerking wordt beschreven, optioneel een aantekening met de bewerkings kenmerken, een open accolade `{` , de hoofd tekst van de bewerkings `}`</span><span class="sxs-lookup"><span data-stu-id="992be-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="992be-113">Elke bewerking neemt een invoer, produceert een uitvoer en geeft de implementatie aan voor een of meer bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="992be-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="992be-114">De mogelijke specials en hoe u deze kunt definiëren/aanroepen, worden verder uitgebreid beschreven.</span><span class="sxs-lookup"><span data-stu-id="992be-114">The possible specializations, and how to define/call them, are detailed further below.</span></span>
<span data-ttu-id="992be-115">Bekijk nu de volgende bewerking, waarmee alleen een standaard hoofd tekst wordt gedefinieerd en waarbij één Qubit als invoer wordt gebruikt. vervolgens wordt de ingebouwde <xref:microsoft.quantum.intrinsic.x> bewerking voor die invoer aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="992be-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="992be-116">Het sleutel woord `operation` begint de definitie van de bewerking en wordt gevolgd door de naam; hier, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="992be-116">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="992be-117">Vervolgens wordt het type van de invoer gedefinieerd als `Qubit` , samen met een naam `target` voor het verwijzen naar de invoer binnen de nieuwe bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-117">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="992be-118">Op dezelfde manier `Unit` wordt met de definitie aangegeven dat de uitvoer van de bewerking leeg is.</span><span class="sxs-lookup"><span data-stu-id="992be-118">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="992be-119">Dit wordt op dezelfde manier gebruikt als `void` in C# en andere verplichte talen en is gelijk aan `unit` in F # en andere functionele talen.</span><span class="sxs-lookup"><span data-stu-id="992be-119">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="992be-120">Bewerkingen kunnen ook interessante typen retour neren dan `Unit` .</span><span class="sxs-lookup"><span data-stu-id="992be-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="992be-121">De <xref:microsoft.quantum.intrinsic.m> bewerking retourneert bijvoorbeeld een uitvoer van het type `Result` , die aangeeft dat een meting is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="992be-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="992be-122">We kunnen de uitvoer van een bewerking door geven aan een andere bewerking of deze gebruiken met het `let` sleutel woord om een nieuwe variabele te definiëren.</span><span class="sxs-lookup"><span data-stu-id="992be-122">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="992be-123">Dit maakt het mogelijk om klassieke berekeningen aan te duiden die met Quantum bewerkingen op een laag niveau reageren, zoals bij de [code ring](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)van de functie:</span><span class="sxs-lookup"><span data-stu-id="992be-123">This allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> <span data-ttu-id="992be-124">Elke bewerking in Q # heeft precies één invoer en retourneert precies één uitvoer.</span><span class="sxs-lookup"><span data-stu-id="992be-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="992be-125">Meerdere invoer en uitvoer worden vervolgens weer gegeven met behulp van *Tuples*, waarbij meerdere waarden worden verzameld in één waarde.</span><span class="sxs-lookup"><span data-stu-id="992be-125">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="992be-126">We zeggen dat Q # een ' tuple-in ' tuple-out ' is.</span><span class="sxs-lookup"><span data-stu-id="992be-126">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="992be-127">Dit concept `()` moet worden gelezen als de ' empty ' tuple, die van het type is `Unit` .</span><span class="sxs-lookup"><span data-stu-id="992be-127">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>


## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="992be-128">Gecontroleerde en adjoint bewerkingen</span><span class="sxs-lookup"><span data-stu-id="992be-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="992be-129">Als een bewerking een unitary-trans formatie implementeert, zoals het geval is voor veel bewerkingen in Q #, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt.</span><span class="sxs-lookup"><span data-stu-id="992be-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="992be-130">Met een *adjoint* specialisatie van een bewerking wordt aangegeven hoe de ' inverse ' van de bewerking wordt uitgevoerd, terwijl een *beheerde* specialisatie aangeeft hoe een bewerking wordt uitgevoerd wanneer de toepassing wordt ingesteld op de status van een bepaalde Quantum register.</span><span class="sxs-lookup"><span data-stu-id="992be-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="992be-131">Adjoints van Quantum bewerkingen zijn cruciaal voor veel aspecten van Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="992be-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="992be-132">Hieronder vindt u in de sectie [Conjugations](#conjugations) een dergelijke situatie die wordt besproken naast een handige Q #-programmeer techniek.</span><span class="sxs-lookup"><span data-stu-id="992be-132">Further below, in the [Conjugations](#conjugations) section, you will find one such situation discussed alongside a useful Q# programming technique.</span></span>

<span data-ttu-id="992be-133">De gecontroleerde versie van een bewerking is een nieuwe bewerking waarbij de basis bewerking alleen effectief wordt toegepast als alle besturings elementen qubits een opgegeven status hebben.</span><span class="sxs-lookup"><span data-stu-id="992be-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="992be-134">Als het besturings element qubits zich in de superpositie bevindt, wordt de basis bewerking samenhangend toegepast op het juiste deel van de superpositie.</span><span class="sxs-lookup"><span data-stu-id="992be-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="992be-135">Daarom worden beheerde bewerkingen vaak gebruikt voor het genereren van Entanglement.</span><span class="sxs-lookup"><span data-stu-id="992be-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="992be-136">Natuurlijk kan ook een *beheerde adjoint* -specialisatie bestaan en de gecontroleerde toepassing van de adjoint van een bewerking opgeven.</span><span class="sxs-lookup"><span data-stu-id="992be-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="992be-137">Als $U $ de unitary-trans formatie is die door een bewerking wordt geïmplementeerd `U` , `Adjoint U` vertegenwoordigt de unitary-trans formatie $U ^ \dagger $, de complex geconjugeerde getransponeerde.</span><span class="sxs-lookup"><span data-stu-id="992be-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="992be-138">Als er een bewerking wordt toegepast en vervolgens de adjoint naar een status, blijft de status ongewijzigd, zoals wordt geïllustreerd door $UU ^ \dagger = U ^ \dagger U = \id $, de identiteits matrix.</span><span class="sxs-lookup"><span data-stu-id="992be-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="992be-139">De unitary-weer gave van een gecontroleerde bewerking is iets ingewik complexer, maar u kunt meer informatie vinden over de [concepten van Quantum Computing: meerdere qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="992be-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="992be-140">In de volgende sectie wordt beschreven hoe u deze verschillende specials aanroept in uw Q #-code.</span><span class="sxs-lookup"><span data-stu-id="992be-140">The following section describes how to call these various specializations in your Q# code.</span></span>
<span data-ttu-id="992be-141">Hieronder vindt u informatie over het definiëren van bewerkingen ter ondersteuning van deze activiteiten.</span><span class="sxs-lookup"><span data-stu-id="992be-141">Below, we detail how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="992be-142">Bewerkings specials aanroepen</span><span class="sxs-lookup"><span data-stu-id="992be-142">Calling operation specializations</span></span>

<span data-ttu-id="992be-143">Een *functor* in Q # is een Factory die een nieuwe bewerking vanuit een andere bewerking definieert.</span><span class="sxs-lookup"><span data-stu-id="992be-143">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="992be-144">De twee standaard functors in Q # zijn `Adjoint` en `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="992be-144">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="992be-145">Functors hebben toegang tot de implementatie van de basis bewerking bij het definiëren van de implementatie van de nieuwe bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-145">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="992be-146">Daarom kunnen functors complexere functies uitvoeren dan traditionele functies op een hoger niveau.</span><span class="sxs-lookup"><span data-stu-id="992be-146">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="992be-147">Functors hebben geen weer gave in het Q #-type systeem.</span><span class="sxs-lookup"><span data-stu-id="992be-147">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="992be-148">Het is dus niet mogelijk om deze aan een variabele te binden of als argumenten door te geven.</span><span class="sxs-lookup"><span data-stu-id="992be-148">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="992be-149">Een functor wordt gebruikt door deze toe te passen op een bewerking en een nieuwe bewerking te retour neren.</span><span class="sxs-lookup"><span data-stu-id="992be-149">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="992be-150">De bewerking die het resultaat is van het Toep assen van de `Adjoint` functor op de `Y` bewerking, wordt bijvoorbeeld als volgt geschreven `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="992be-150">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="992be-151">De nieuwe bewerking kan vervolgens worden aangeroepen, zoals elke andere bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-151">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="992be-152">Voor een bewerking ter ondersteuning van de toepassing van de `Adjoint` en/of `Controlled` functors moet het retour type daarvan nood zakelijk zijn `Unit` .</span><span class="sxs-lookup"><span data-stu-id="992be-152">For an operation to support application of the `Adjoint` and/or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="992be-153">`Adjoint`functor</span><span class="sxs-lookup"><span data-stu-id="992be-153">`Adjoint` functor</span></span>

<span data-ttu-id="992be-154">`Adjoint Y(q1)`Op die manier wordt de adjoint functor toegepast op de `Y` bewerking om een nieuwe bewerking te genereren en wordt deze nieuwe bewerking toegepast op `q1` .</span><span class="sxs-lookup"><span data-stu-id="992be-154">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="992be-155">De nieuwe bewerking heeft dezelfde hand tekening en type als de basis bewerking `Y` .</span><span class="sxs-lookup"><span data-stu-id="992be-155">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="992be-156">Met name de nieuwe bewerking staat ook `Adjoint` toe en is alleen toegestaan als `Controlled` de basis bewerking is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="992be-156">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="992be-157">De adjoint-functor is zijn eigen inverse; dat wil zeggen, `Adjoint Adjoint Op` is altijd hetzelfde als `Op` .</span><span class="sxs-lookup"><span data-stu-id="992be-157">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="992be-158">`Controlled`functor</span><span class="sxs-lookup"><span data-stu-id="992be-158">`Controlled` functor</span></span>

<span data-ttu-id="992be-159">Op dezelfde manier wordt `Controlled X(controls, target)` de beheerde functor toegepast op de `X` bewerking voor het genereren van een nieuwe bewerking en wordt die nieuwe bewerking toegepast op `controls` en `target` .</span><span class="sxs-lookup"><span data-stu-id="992be-159">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="992be-160">In Q # maken bewaakte versies altijd een matrix van besturings element qubits en de opgegeven status is altijd voor alle besturings elementen qubits in de status berekening ( `PauliZ` ) `One` , $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="992be-160">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="992be-161">Het beheer op basis van andere Staten kan worden bereikt door de juiste unitary-bewerking toe te passen op de controle qubits vóór de gecontroleerde bewerking en vervolgens de inverse van de unitary-bewerking toe te passen na de gecontroleerde bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-161">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="992be-162">Als u bijvoorbeeld een `X` bewerking toepast op een besturings element Qubit vóór en na een beheerde bewerking, wordt de bewerking voor het beheren van de `Zero` status ($ \ket {0} $) voor die Qubit uitgevoerd. het Toep assen van een `H` bewerking voor en na heeft tot gevolg `PauliX` `One` dat-1 eigenvalue van Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ in plaats van de `PauliZ` `One` status.</span><span class="sxs-lookup"><span data-stu-id="992be-162">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="992be-163">Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="992be-163">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="992be-164">De hand tekening van de nieuwe bewerking is gebaseerd op de hand tekening van de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-164">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="992be-165">Het resultaat type is hetzelfde, maar het invoer type is een twee-tuple met een Qubit-matrix met de Qubit (s) die het eerste element bevat en de argumenten van de oorspronkelijke bewerking als het tweede element.</span><span class="sxs-lookup"><span data-stu-id="992be-165">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="992be-166">De nieuwe bewerking ondersteunt `Controlled` , en wordt alleen ondersteund als `Adjoint` de oorspronkelijke bewerking is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="992be-166">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="992be-167">Als de oorspronkelijke bewerking slechts één argument heeft gevolgd, komt de singleton-tuple-equivalentie hier te staan.</span><span class="sxs-lookup"><span data-stu-id="992be-167">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="992be-168">Bijvoorbeeld, `Controlled X` is de beheerde versie van de `X` bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-168">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="992be-169">`X`heeft type `(Qubit => Unit is Adj + Ctl)` , dus `Controlled X` heeft type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; vanwege Singleton-tuple-equivalentie is dit hetzelfde als `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="992be-169">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="992be-170">Als de basis bewerking meerdere argumenten heeft, moet u de overeenkomstige argumenten van de gecontroleerde versie van de bewerking tussen haakjes plaatsen om ze te converteren naar een tuple.</span><span class="sxs-lookup"><span data-stu-id="992be-170">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="992be-171">Bijvoorbeeld, `Controlled Rz` is de beheerde versie van de `Rz` bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-171">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="992be-172">`Rz`heeft type `((Double, Qubit) => Unit is Adj + Ctl)` , dus `Controlled Rz` heeft type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="992be-172">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="992be-173">Dit is dus `Controlled Rz(controls, (0.1, target))` een geldige aanroep van `Controlled Rz` (Let op de haakjes rond `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="992be-173">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="992be-174">Een ander voor beeld `CNOT(control, target)` kan worden geïmplementeerd als `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="992be-174">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="992be-175">Als een doel moet worden beheerd door 2 Control qubits (CCNOT), kunnen we de `Controlled X([control1, control2], target)` instructie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="992be-175">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="992be-176">Het `Controlled` en `Adjoint` functors werk, dus er is geen verschil tussen het Toep assen van `Controlled Adjoint Op` of `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="992be-176">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="992be-177">Beheerde en adjoint-implementaties definiëren</span><span class="sxs-lookup"><span data-stu-id="992be-177">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="992be-178">In de eerste voor beelden van bewerkings declaraties zijn de bewerkingen `BitFlip` en `DecodeSuperdense` zijn gedefinieerd met hand tekeningen `(Qubit => Unit)` en `((Qubit, Qubit) => (Result, Result))` respectievelijk.</span><span class="sxs-lookup"><span data-stu-id="992be-178">In the first operation declaration examples above, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="992be-179">Net als bij `DecodeSuperdense` metingen, is het geen unitary-bewerking en zijn er geen beheerde niet-adjointe specials mogelijk (roep de gerelateerde vereiste in die een dergelijke bewerking retourneert `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="992be-179">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="992be-180">Als `BitFlip` simpelweg de unitary <xref:microsoft.quantum.intrinsic.x> -bewerking uitvoert, kunnen we deze echter wel met beide specials hebben gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="992be-180">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, we could have defined it with both specializations.</span></span>

<span data-ttu-id="992be-181">Hier wordt beschreven hoe u het bestaan van specials in uw Q #-bewerkings declaraties opneemt, zodat ze kunnen worden aangeroepen in combi natie met de `Adjoint` en/of `Controlled` functors.</span><span class="sxs-lookup"><span data-stu-id="992be-181">Here, we detail how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` and/or `Controlled` functors.</span></span>
<span data-ttu-id="992be-182">[Hieronder](#circumstances-for-validly-defining-specializations)worden enkele situaties beschreven waarin het geldig is of niet geldig is voor het declareren van bepaalde specials.</span><span class="sxs-lookup"><span data-stu-id="992be-182">Further [below](#circumstances-for-validly-defining-specializations), we describe some of the situations in which it is either valid or not valid to declare certain specializations.</span></span>

<span data-ttu-id="992be-183">Met bewerkings kenmerken wordt gedefinieerd welke soorten functors kunnen worden toegepast op de gedeclareerde bewerking en welk effect ze hebben.</span><span class="sxs-lookup"><span data-stu-id="992be-183">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="992be-184">Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking, met name door een aantekening met de bewerkings kenmerken: ofwel `is Adj` , `is Ctl` of `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="992be-184">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="992be-185">De daad werkelijke implementatie van elke specialisatie kan *impliciet* of *expliciet* worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="992be-185">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="992be-186">Impliciete implementaties opgeven</span><span class="sxs-lookup"><span data-stu-id="992be-186">Implicitly specifying implementations</span></span>

<span data-ttu-id="992be-187">In dit geval bestaat de hoofd tekst van de bewerkings declaratie uit uitsluitend de standaard implementatie.</span><span class="sxs-lookup"><span data-stu-id="992be-187">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="992be-188">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="992be-188">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="992be-189">Hier wordt de overeenkomstige implementatie voor elke impliciet gedeclareerde specialisatie automatisch gegenereerd door de compiler om te worden uitgevoerd als de `Adjoint` of `Controlled` functors wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="992be-189">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="992be-190">Daarom zou een aanroep van `Adjoint PrepareEntangledPair` zouden leiden tot het compileren van de adjoint van `CNOT` en vervolgens de adjoint van `H` .</span><span class="sxs-lookup"><span data-stu-id="992be-190">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="992be-191">Deze afzonderlijke bewerkingen zijn beide Self-adjoint, dus de resulterende `Adjoint PrepareEntangledPair` bewerking zou gewoon bestaan `CNOT(here, there)` en vervolgens worden toegepast `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="992be-191">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="992be-192">Daarom kunnen we dit gebruiken om het `DecodeSuperdense` bovenstaande voor beeld sneller te schrijven, met behulp van de adjoint van `PrepareEntangledPair` om de Entangled-status terug te zetten in een unentangled paar qubits:</span><span class="sxs-lookup"><span data-stu-id="992be-192">Hence we can use this to write the `DecodeSuperdense` example above more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="992be-193">De aantekening met de bewerkings kenmerken in de declaratie is handig om ervoor te zorgen dat de compiler automatisch andere specials wordt gegenereerd op basis van de standaard implementatie.</span><span class="sxs-lookup"><span data-stu-id="992be-193">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="992be-194">Er zijn een aantal belang rijke beperkingen waarmee u rekening moet houden bij het ontwerpen van bewerkingen voor gebruik met functors.</span><span class="sxs-lookup"><span data-stu-id="992be-194">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="992be-195">De meeste van de voor delen van een bewerking die de uitvoer waarde van een andere bewerking gebruikt, *kan niet* automatisch worden gegenereerd door de compiler, omdat het niet eenduidig is hoe u de instructies in een dergelijke bewerking opnieuw ordent om hetzelfde effect te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="992be-195">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="992be-196">Daarom is het vaak handig om de verschillende implementaties expliciet op te geven.</span><span class="sxs-lookup"><span data-stu-id="992be-196">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="992be-197">Expliciet opgeven van implementaties</span><span class="sxs-lookup"><span data-stu-id="992be-197">Explicitly specifying implementations</span></span>

<span data-ttu-id="992be-198">Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="992be-198">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="992be-199">Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte instructie voor het *genereren* of een door de gebruiker gedefinieerde implementatie.</span><span class="sxs-lookup"><span data-stu-id="992be-199">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="992be-200">Hier bieden we het volledige aanbod van mogelijkheden, met voor beelden hieronder.</span><span class="sxs-lookup"><span data-stu-id="992be-200">Here we provide the full range of possibilities, with examples following below.</span></span>


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="992be-201">Expliciete specialisatie declaraties</span><span class="sxs-lookup"><span data-stu-id="992be-201">Explicit specialization declarations</span></span>

<span data-ttu-id="992be-202">Q #-bewerkingen kunnen de volgende expliciete specialisatie declaraties bevatten:</span><span class="sxs-lookup"><span data-stu-id="992be-202">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="992be-203">De `body` specialisatie specificeert de implementatie van de bewerking waarvoor geen functors is toegepast.</span><span class="sxs-lookup"><span data-stu-id="992be-203">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="992be-204">De `adjoint` specialisatie specificeert de implementatie van de bewerking waarop de `Adjoint` functor is toegepast.</span><span class="sxs-lookup"><span data-stu-id="992be-204">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="992be-205">De `controlled` specialisatie specificeert de implementatie van de bewerking waarop de `Controlled` functor is toegepast.</span><span class="sxs-lookup"><span data-stu-id="992be-205">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="992be-206">De `controlled adjoint` specialisatie specificeert de implementatie van de bewerking waarbij de `Adjoint` en `Controlled` functors zijn toegepast.</span><span class="sxs-lookup"><span data-stu-id="992be-206">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="992be-207">Deze specialisatie kan ook worden genoemd `adjoint controlled` , omdat de twee functors werkend zijn.</span><span class="sxs-lookup"><span data-stu-id="992be-207">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="992be-208">Een specialisatie bewerking bestaat uit het specialisatie label (bijvoorbeeld `body` of `adjoint` , enzovoort), gevolgd door een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="992be-208">An operation specialization consists of the specialization tag (e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="992be-209">Een expliciete declaratie zoals hieronder wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="992be-209">An explicit declaration as described below.</span></span>
- <span data-ttu-id="992be-210">Een *instructie* die de compiler vertelt *hoe* de specialisatie moet worden gegenereerd, een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="992be-210">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="992be-211">`intrinsic`. Dit geeft aan dat de specialisatie wordt verschaft door de doel computer.</span><span class="sxs-lookup"><span data-stu-id="992be-211">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="992be-212">`distribute`, die kunnen worden gebruikt met de `controlled` en `controlled adjoint` specials.</span><span class="sxs-lookup"><span data-stu-id="992be-212">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="992be-213">Bij gebruik met `controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door toe `Controlled` te passen op alle bewerkingen in de `body` .</span><span class="sxs-lookup"><span data-stu-id="992be-213">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="992be-214">Bij gebruik met `controlled adjoint` geeft dit aan dat de compiler de specialisatie moet berekenen door `Controlled` alle bewerkingen in de specialisatie toe te passen `adjoint` .</span><span class="sxs-lookup"><span data-stu-id="992be-214">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="992be-215">`invert`Dit geeft aan dat de compiler de `adjoint` specialisatie moet berekenen door de `body` , dat wil zeggen de volg orde van de bewerkingen en het Toep assen van de adjoint op elke waarde.</span><span class="sxs-lookup"><span data-stu-id="992be-215">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="992be-216">Bij gebruik met `adjoint controlled` geeft dit aan dat de compiler de specialisatie moet berekenen door de specialisatie te omkeren `controlled` .</span><span class="sxs-lookup"><span data-stu-id="992be-216">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="992be-217">`self`om aan te geven dat de adjoint specialize hetzelfde is als de `body` specialisatie.</span><span class="sxs-lookup"><span data-stu-id="992be-217">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="992be-218">Dit is juridisch voor de `adjoint` en `adjoint controlled` specials.</span><span class="sxs-lookup"><span data-stu-id="992be-218">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="992be-219">Voor `adjoint controlled` `self` betekent dat de `adjoint controlled` specialisatie hetzelfde is als de `controlled` specialisatie.</span><span class="sxs-lookup"><span data-stu-id="992be-219">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="992be-220">`auto`om aan te geven dat de compiler een geschikte richt lijn moet selecteren om toe te passen.</span><span class="sxs-lookup"><span data-stu-id="992be-220">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="992be-221">`auto`kan niet worden gebruikt voor de `body` specialisatie.</span><span class="sxs-lookup"><span data-stu-id="992be-221">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="992be-222">De richt lijnen en `auto` alle vereisen een sluitende punt komma `;` .</span><span class="sxs-lookup"><span data-stu-id="992be-222">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="992be-223">De `auto` instructie wordt omgezet in de volgende generatie-instructie als een expliciete declaratie van de `body` wordt gegeven:</span><span class="sxs-lookup"><span data-stu-id="992be-223">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="992be-224">De `adjoint` specialisatie wordt gegenereerd volgens de instructie `invert` .</span><span class="sxs-lookup"><span data-stu-id="992be-224">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="992be-225">De `controlled` specialisatie wordt gegenereerd volgens de instructie `distribute` .</span><span class="sxs-lookup"><span data-stu-id="992be-225">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="992be-226">De `adjoint controlled` specialisatie wordt gegenereerd volgens de richt lijn `invert` als een expliciete declaratie voor `controlled` is opgegeven, maar niet een voor `adjoint` , en `distribute` anders.</span><span class="sxs-lookup"><span data-stu-id="992be-226">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="992be-227">Als een bewerking zelf adjoint is, geeft u expliciet de adjoint of de bewaakte adjoint-specialisatie op via de generatie-instructie `self` zodat de compiler gebruik van die informatie kan maken voor optimaliserings doeleinden.</span><span class="sxs-lookup"><span data-stu-id="992be-227">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="992be-228">Een specialisatie declaratie met een door de gebruiker gedefinieerde implementatie bestaat uit een argument tuple gevolgd door een instructie blok met de Q #-code die de specialisatie implementeert.</span><span class="sxs-lookup"><span data-stu-id="992be-228">A specialization declaration containing a user-defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="992be-229">In de argumenten lijst `...` wordt gebruikt om de argumenten weer te geven die zijn gedeclareerd voor de bewerking als geheel.</span><span class="sxs-lookup"><span data-stu-id="992be-229">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="992be-230">Voor `body` en `adjoint` , de lijst met argumenten moet altijd zijn `(...)` : voor `controlled` en `adjoint controlled` , de lijst met argumenten moet een symbool zijn dat de matrix van besturings element qubits, gevolgd door `...` , tussen haakjes (bijvoorbeeld) `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="992be-230">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="992be-231">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="992be-231">Examples</span></span>

<span data-ttu-id="992be-232">Een bewerkings declaratie kan zo eenvoudig zijn als het volgende, wat de primitieve Pauli X-bewerking definieert:</span><span class="sxs-lookup"><span data-stu-id="992be-232">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="992be-233">Houd er rekening mee dat de adjoint van de Pauli X-bewerking is gedefinieerd met de instructie, `self` omdat de `X` eigen inverse van de definitie.</span><span class="sxs-lookup"><span data-stu-id="992be-233">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="992be-234">De bovenstaande code `PrepareEntangledPair` is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie:</span><span class="sxs-lookup"><span data-stu-id="992be-234">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="992be-235">Het sleutel woord `auto` geeft aan dat de compiler moet bepalen hoe u de implementatie van de specialisatie wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="992be-235">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="992be-236">Door de gebruiker gedefinieerde implementatie van specialisatie</span><span class="sxs-lookup"><span data-stu-id="992be-236">User-defined specialization implementation</span></span>

<span data-ttu-id="992be-237">Als de compiler de implementatie voor een bepaalde specialisatie niet automatisch kan genereren of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="992be-237">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="992be-238">In het bovenstaande voor beeld `adjoint invert;` geeft aan dat de adjoint-specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie te omkeren.</span><span class="sxs-lookup"><span data-stu-id="992be-238">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="992be-239">Als een of meer specialisaties naast de standaard hoofd tekst expliciet moeten worden gedeclareerd, moet de implementatie voor de standaard hoofd tekst ook worden ingepakt in een geschikte specialisatie declaratie.</span><span class="sxs-lookup"><span data-stu-id="992be-239">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="992be-240">Omstandigheden voor het op geldige wijze definiëren van specials</span><span class="sxs-lookup"><span data-stu-id="992be-240">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="992be-241">Bewerkings declaraties met adjoint/beheerd</span><span class="sxs-lookup"><span data-stu-id="992be-241">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="992be-242">Het is wettelijk om een bewerking zonder adjoint of beheerde versies op te geven.</span><span class="sxs-lookup"><span data-stu-id="992be-242">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="992be-243">Meting bewerkingen hebben bijvoorbeeld geen, omdat ze niet omkeerbaar of niet kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="992be-243">For instance, measurement operations have neither, because they are not invertible or controllable.</span></span>

<span data-ttu-id="992be-244">Een bewerking ondersteunt de `Adjoint` en/of `Controlled` functors als de bijbehorende declaratie een impliciete of expliciete declaratie van de respectieve specials bevat.</span><span class="sxs-lookup"><span data-stu-id="992be-244">An operation supports the `Adjoint` and/or `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="992be-245">Een expliciet aangegeven adjoint/beheerde specialisatie impliceert dat er een adjoint/beheerde specialisatie bestaat.</span><span class="sxs-lookup"><span data-stu-id="992be-245">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="992be-246">Voor een bewerking waarvan de hoofd tekst herhalen-until-success-lussen, set-instructies, metingen, retour overzichten of aanroepen naar andere bewerkingen die de functor niet ondersteunen `Adjoint` , het automatisch genereren van een adjoint-specialisatie volgens de `invert` or- `auto` instructie is niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="992be-246">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="992be-247">Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen ondersteuning bieden voor de `Controlled` functor, wordt het automatisch genereren van een gecontroleerde specialisatie volgens de `distribute` or- `auto` instructie niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="992be-247">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="992be-248">Beheerde adjoint</span><span class="sxs-lookup"><span data-stu-id="992be-248">Controlled Adjoint</span></span>

<span data-ttu-id="992be-249">De gecontroleerde adjoint-versie van een bewerking geeft aan hoe een Quantum versie van de adjoint van de bewerking wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="992be-249">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="992be-250">Het is niet toegestaan een bewerking op te geven zonder beheerde adjoint-versie. meting bewerkingen hebben bijvoorbeeld geen beheerde adjoint-versie omdat ze niet kunnen worden ingesteld of omkeerbaar.</span><span class="sxs-lookup"><span data-stu-id="992be-250">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="992be-251">Een beheerde adjoint-specialisatie voor een bewerking moet bestaan als en alleen als zowel een adjoint als een beheerde specialisatie bestaan.</span><span class="sxs-lookup"><span data-stu-id="992be-251">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="992be-252">In dat geval wordt het bestaan van de beheerde adjoint-specialisatie afgeleid en wordt er een geschikte specialisatie gegenereerd door de compiler als er expliciet geen implementatie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="992be-252">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="992be-253">Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen beheerde adjoint-versie hebben, wordt het automatisch genereren van een adjoint specialisatie na de `invert` `distribute` of- `auto` instructie niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="992be-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="992be-254">Type compatibiliteit</span><span class="sxs-lookup"><span data-stu-id="992be-254">Type Compatibility</span></span>

<span data-ttu-id="992be-255">Een bewerking met aanvullende functors-ondersteuning kan worden gebruikt op een wille keurige locatie met minder functors, maar dezelfde hand tekening wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="992be-255">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="992be-256">Een bewerking van het type kan bijvoorbeeld `(Qubit => Unit is Adj)` worden gebruikt overal een bewerking van het type `(Qubit => Unit)` wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="992be-256">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="992be-257">Q # is *covariantie* ten opzichte van aanroep bare retour typen: een aanroepable die een type retourneert `'A` , is compatibel met een aanroepbaar met hetzelfde invoer type en een resultaat type dat `'A` compatibel is met.</span><span class="sxs-lookup"><span data-stu-id="992be-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="992be-258">Q # is *contra variant* met betrekking tot invoer typen: een aanroepable die een type `'A` als invoer vereist, is compatibel met een aanroepbaar met hetzelfde resultaat type en een invoer type dat compatibel is met `'A` .</span><span class="sxs-lookup"><span data-stu-id="992be-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="992be-259">Dat wil zeggen, op basis van de volgende definities:</span><span class="sxs-lookup"><span data-stu-id="992be-259">That is, given the following definitions:</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="992be-260">de volgende voor waarden zijn waar:</span><span class="sxs-lookup"><span data-stu-id="992be-260">the following are true:</span></span>

- <span data-ttu-id="992be-261">De functie `ConjugateInvertWith` kan worden aangeroepen met een `inner` argument van ofwel `Invert` of `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="992be-261">The function `ConjugateInvertWith` may be invoked with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="992be-262">De functie `ConjugateUnitaryWith` kan worden aangeroepen met een `inner` argument van `ApplyUnitary` , maar niet `Invert` .</span><span class="sxs-lookup"><span data-stu-id="992be-262">The function `ConjugateUnitaryWith` may be invoked with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="992be-263">Er kan een waarde van het type `(Qubit[] => Unit is Adj + Ctl)` worden geretourneerd van `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="992be-263">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="992be-264">Q # 0,3 heeft een aanzienlijk verschil in het gedrag van door de gebruiker gedefinieerde typen geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="992be-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="992be-265">Door de gebruiker gedefinieerde typen worden behandeld als een ingepakte versie van het onderliggende type, in plaats van als subtype.</span><span class="sxs-lookup"><span data-stu-id="992be-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="992be-266">Dit betekent dat een waarde van een door de gebruiker gedefinieerd type niet kan worden gebruikt als een waarde van het onderliggende type wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="992be-266">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>


### <a name="conjugations"></a><span data-ttu-id="992be-267">Conjugations</span><span class="sxs-lookup"><span data-stu-id="992be-267">Conjugations</span></span>

<span data-ttu-id="992be-268">In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn.</span><span class="sxs-lookup"><span data-stu-id="992be-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="992be-269">Dit kan worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="992be-269">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="992be-270">Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende:</span><span class="sxs-lookup"><span data-stu-id="992be-270">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="992be-271">Vanaf onze 0,9-release ondersteunen we een conjugation-instructie die de bovenstaande trans formatie implementeert.</span><span class="sxs-lookup"><span data-stu-id="992be-271">Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="992be-272">Met deze instructie kan de bewerking `ApplyWith` op de volgende manier worden geïmplementeerd:</span><span class="sxs-lookup"><span data-stu-id="992be-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="992be-273">Een dergelijke conjugation-instructie is natuurlijk veel handiger als de buitenste en de binnenste trans formatie niet onmiddellijk beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies.</span><span class="sxs-lookup"><span data-stu-id="992be-273">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="992be-274">De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid.</span><span class="sxs-lookup"><span data-stu-id="992be-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span>
<span data-ttu-id="992be-275">Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok.</span><span class="sxs-lookup"><span data-stu-id="992be-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="992be-276">Nieuwe functies definiëren</span><span class="sxs-lookup"><span data-stu-id="992be-276">Defining New Functions</span></span>

<span data-ttu-id="992be-277">Functions zijn louter deterministische, klassieke routines in Q #, die verschillend zijn van bewerkingen in dat ze geen invloed mogen hebben op de berekening van een uitvoer waarde.</span><span class="sxs-lookup"><span data-stu-id="992be-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="992be-278">Met name functies kunnen geen bewerkingen aanroepen; actie ondernemen, toewijzen of lenen qubits; voor beelden van wille keurige getallen; of op andere wijze, afhankelijk van de invoer waarde voor een functie.</span><span class="sxs-lookup"><span data-stu-id="992be-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="992be-279">Als gevolg hiervan zijn Q #-functies *puur*, in dat ze altijd dezelfde invoer waarden toewijzen aan dezelfde uitvoer waarden.</span><span class="sxs-lookup"><span data-stu-id="992be-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="992be-280">Hiermee kan de Q #-compiler veilig de volg orde wijzigen van hoe en wanneer-functies worden aangeroepen bij het genereren van bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="992be-280">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="992be-281">Elk Q #-bron bestand kan een wille keurig aantal functies definiëren.</span><span class="sxs-lookup"><span data-stu-id="992be-281">Each Q# source file may define any number of functions.</span></span>
<span data-ttu-id="992be-282">Functie namen moeten uniek zijn binnen een naam ruimte en kunnen een conflict veroorzaken met bewerkingen of type namen.</span><span class="sxs-lookup"><span data-stu-id="992be-282">Function names must be unique within a namespace and may not conflict with operation or type names.</span></span>

<span data-ttu-id="992be-283">Het definiëren van een functie werkt op dezelfde manier als het definiëren van een bewerking, behalve dat er geen adjoint of beheerde Specials kunnen worden gedefinieerd voor een functie.</span><span class="sxs-lookup"><span data-stu-id="992be-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="992be-284">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="992be-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="992be-285">of</span><span class="sxs-lookup"><span data-stu-id="992be-285">or</span></span> 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="992be-286">Klassieke logica in functions = = goed</span><span class="sxs-lookup"><span data-stu-id="992be-286">Classical logic in functions == good</span></span>

<span data-ttu-id="992be-287">Wanneer het mogelijk is om dit te doen, is het handig om klassieke logica te schrijven in termen van functies in plaats van bewerkingen, zodat deze gemakkelijk vanuit bewerkingen kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="992be-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="992be-288">Als we bijvoorbeeld de bovenstaande declaratie hebben geschreven `Square` als een *bewerking*, zou de compiler niet kunnen garanderen dat het aanroepen van deze met dezelfde invoer consequent dezelfde uitvoer produceert.</span><span class="sxs-lookup"><span data-stu-id="992be-288">For example, if we had written the `Square` declaration above as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="992be-289">Als u het verschil tussen functies en bewerkingen wilt onderstrepen, moet u rekening houden met het probleem van klassieke steek proeven voor een wille keurig getal in een Q #-bewerking:</span><span class="sxs-lookup"><span data-stu-id="992be-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="992be-290">Elke keer dat `U` wordt aangeroepen, heeft het een andere actie `target` .</span><span class="sxs-lookup"><span data-stu-id="992be-290">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="992be-291">In het bijzonder kan de compiler niet garanderen dat als we een `adjoint auto` specialisatie-declaratie aan hebben toegevoegd `U` , vervolgens `U(target); Adjoint U(target);` fungeren als identiteit (dat wil zeggen, als niet op).</span><span class="sxs-lookup"><span data-stu-id="992be-291">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="992be-292">Dit schendt de definitie van de adjoint die we hebben gezien in [vectoren en matrices](xref:microsoft.quantum.concepts.vectors), waardoor het automatisch genereren van een adjoint-specialisatie in een bewerking waarbij de bewerking werd aangeroepen, <xref:microsoft.quantum.math.randomreal> de door de compiler geboden garanties zou verstoren; <xref:microsoft.quantum.math.randomreal> is een bewerking waarvoor geen adjoint of gecontroleerde versie bestaat.</span><span class="sxs-lookup"><span data-stu-id="992be-292">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="992be-293">Aan de andere kant, waardoor functie aanroepen zoals `Square` veilig kunnen worden uitgevoerd, kan worden gegarandeerd dat de compiler alleen de invoer moet behouden om de `Square` uitvoer stabiel te houden.</span><span class="sxs-lookup"><span data-stu-id="992be-293">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="992be-294">Door zo veel mogelijk klassieke logica in functies te isoleren, is het eenvoudig om die logica in andere functies en bewerkingen hetzelfde te hergebruiken.</span><span class="sxs-lookup"><span data-stu-id="992be-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="992be-295">Algemene Callables (type parameters)</span><span class="sxs-lookup"><span data-stu-id="992be-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="992be-296">Veel functies en bewerkingen die u mogelijk wilt definiëren, zijn niet echt afhankelijk van de typen invoer, maar u kunt de typen echter alleen impliciet gebruiken via een andere functie of bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-296">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="992be-297">Stel dat het *kaart* concept gebruikelijk is in veel functionele talen. op basis van een functie $f (x) $ en een verzameling waarden $ \{ x_1, x_2, \dots, x_n \} $, kaart retourneert een nieuwe verzameling $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.</span><span class="sxs-lookup"><span data-stu-id="992be-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="992be-298">Om dit in Q # te implementeren, kunnen we profiteren van die functies de eerste klasse.</span><span class="sxs-lookup"><span data-stu-id="992be-298">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="992be-299">We gaan een snel voor beeld van `Map` maken, met ★ als tijdelijke aanduiding, terwijl we weten wat voor typen we nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="992be-299">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="992be-300">Houd er rekening mee dat deze functie veel hetzelfde lijkt, ongeacht de werkelijke typen die we vervangen.</span><span class="sxs-lookup"><span data-stu-id="992be-300">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="992be-301">Een kaart van gehele getallen tot Paulis, bijvoorbeeld ziet er ongeveer hetzelfde uit als een kaart van drijvende-komma getallen naar teken reeksen:</span><span class="sxs-lookup"><span data-stu-id="992be-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="992be-302">In principe zou we een versie van kunnen schrijven `Map` voor elk paar typen dat we tegen komen, maar dit heeft een aantal problemen.</span><span class="sxs-lookup"><span data-stu-id="992be-302">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="992be-303">Als we bijvoorbeeld een bug in hebben gevonden `Map` , moeten we ervoor zorgen dat de oplossing op uniforme wijze wordt toegepast in alle versies van `Map` .</span><span class="sxs-lookup"><span data-stu-id="992be-303">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="992be-304">Als we een nieuwe tuple of UDT bouwen, moeten we nu ook een nieuwe `Map` combi natie maken met het nieuwe type.</span><span class="sxs-lookup"><span data-stu-id="992be-304">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="992be-305">Hoewel dit kan worden beperkt door een klein aantal dergelijke functies, omdat we meer en meer functies van hetzelfde formulier verzamelen, worden `Map` de kosten van het introduceren van nieuwe typen onredelijk groot in een redelijk korte volg orde.</span><span class="sxs-lookup"><span data-stu-id="992be-305">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="992be-306">Veel van deze problemen kunnen er echter toe leiden dat we de compiler niet hebben gezien de informatie die nodig is om te bepalen hoe de verschillende versies van `Map` zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="992be-306">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="992be-307">Effectief moeten we de compiler behandelen `Map` als een soort wiskundige functie van q #- *typen* naar q #-functies.</span><span class="sxs-lookup"><span data-stu-id="992be-307">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="992be-308">Dit principe wordt formeel door het toestaan van functies en bewerkingen om *type parameters*te hebben, evenals de normale tuple-para meters.</span><span class="sxs-lookup"><span data-stu-id="992be-308">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="992be-309">In de bovenstaande voor beelden willen we nadenken over `Map` de typen para meters `Int, Pauli` in het eerste geval en `Double, String` in het tweede geval.</span><span class="sxs-lookup"><span data-stu-id="992be-309">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="992be-310">In het algemeen kunnen deze type parameters vervolgens worden gebruikt alsof het normale typen zijn: we gebruiken waarden van het type para meters om matrices en Tuples te maken, functies en bewerkingen aan te roepen en toe te wijzen aan gewone of onveranderlijke variabelen.</span><span class="sxs-lookup"><span data-stu-id="992be-310">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="992be-311">Het meest extreme geval van indirecte afhankelijkheid is die van qubits, waarbij een Q #-programma niet rechtstreeks kan vertrouwen op de structuur van het `Qubit` type, maar **moet** dergelijke typen door geven aan andere bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="992be-311">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="992be-312">Als u terugkeert naar het bovenstaande voor beeld, kunnen we zien dat we `Map` type-para meters moeten hebben, een voor de invoer tot `fn` en met één om de uitvoer van weer te geven `fn` .</span><span class="sxs-lookup"><span data-stu-id="992be-312">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="992be-313">In Q # wordt dit geschreven door punt haken (dat wil zeggen `<>` , niet brakets $ \braket $!) toe te voegen {} na de naam van een functie of bewerking in de declaratie en door elke type parameter te vermelden.</span><span class="sxs-lookup"><span data-stu-id="992be-313">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="992be-314">De naam van elke type parameter moet beginnen met een streepje `'` , wat aangeeft dat het een type parameter is en niet een normaal type (ook wel een *concreet* type genoemd).</span><span class="sxs-lookup"><span data-stu-id="992be-314">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="992be-315">Voor kunnen `Map` we het volgende schrijven:</span><span class="sxs-lookup"><span data-stu-id="992be-315">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="992be-316">Houd er rekening mee dat de definitie van een `Map<'Input, 'Output>` uitermate gelijkenis lijkt met de versies die we eerder hebben afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="992be-316">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="992be-317">Het enige verschil is dat we het Compileer programma expliciet hebben geïnformeerd dat `Map` niet rechtstreeks afhankelijk is van wat en dat wel `'Input` `'Output` , maar wel voor twee typen, met behulp van deze indirect via `fn` .</span><span class="sxs-lookup"><span data-stu-id="992be-317">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="992be-318">Zodra we `Map<'Input, 'Output>` op deze manier zijn gedefinieerd, kunnen we deze aanroepen alsof het een gewone functie was:</span><span class="sxs-lookup"><span data-stu-id="992be-318">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="992be-319">Het schrijven van algemene functies en bewerkingen is een plek waar ' tuple-in ' tuple-out ' een zeer handige manier is om te denken over Q #-functies en-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="992be-319">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="992be-320">Omdat voor elke functie precies één invoer wordt gebruikt en er precies één uitvoer wordt geretourneerd, komt een invoer van het type `'T -> 'U` overeen met *elke* Q #-functie.</span><span class="sxs-lookup"><span data-stu-id="992be-320">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="992be-321">Elke bewerking kan ook worden door gegeven aan een invoer van het type `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="992be-321">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="992be-322">Als tweede voor beeld moet u de uitdaging van het schrijven van een functie die de samen stelling van twee andere functies retourneert, overwegen:</span><span class="sxs-lookup"><span data-stu-id="992be-322">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="992be-323">Hier moeten we precies opgeven wat `A` , `B` en `C` zijn, waardoor het hulp programma van onze nieuwe functie ernstig wordt beperkt `Compose` .</span><span class="sxs-lookup"><span data-stu-id="992be-323">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="992be-324">Daarna `Compose` is alleen afhankelijk van `A` , `B` en `C` *via* `innerFn` en `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="992be-324">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="992be-325">Als alternatief kunnen we type parameters toevoegen aan `Compose` die aangeven dat het werkt voor *elk* `A` , `B` en, `C` zolang deze para meters overeenkomen met de verwachte `innerFn` en `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="992be-325">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="992be-326">De standaard bibliotheken van Q # bieden een reeks dergelijke bewerkingen en functies van type para meters waarmee de controle stroom van een hogere volg orde eenvoudiger kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="992be-326">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="992be-327">Deze worden verder besproken in de [hand leiding Q # Standard Library](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="992be-327">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="992be-328">Callables als waarden voor de eerste klasse</span><span class="sxs-lookup"><span data-stu-id="992be-328">Callables as First-Class Values</span></span>

<span data-ttu-id="992be-329">Een van de essentiële technieken voor het opwegen van de controle stroom en klassieke logica met behulp van functies in plaats van bewerkingen is het gebruik van die bewerkingen en functies in Q # zijn de *eerste klasse*.</span><span class="sxs-lookup"><span data-stu-id="992be-329">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="992be-330">Dat wil zeggen dat ze elke waarde in de taal in hun eigen recht zijn.</span><span class="sxs-lookup"><span data-stu-id="992be-330">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="992be-331">Het volgende is bijvoorbeeld een zeer geldige Q #-code, als een beetje indirect:</span><span class="sxs-lookup"><span data-stu-id="992be-331">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="992be-332">De waarde van de variabele `ourH` in het bovenstaande fragment is vervolgens de bewerking <xref:microsoft.quantum.intrinsic.h> , zodat we deze waarde kunnen aanroepen, zoals elke andere bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-332">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="992be-333">Hierdoor kunnen we bewerkingen schrijven die bewerkingen als onderdeel van hun invoer doen, waardoor de controle stroom concepten met een hogere volg orde kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="992be-333">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="992be-334">We kunnen bijvoorbeeld Voorst Ellen om een bewerking te ' Square ' door deze twee keer op dezelfde doel-Qubit toe te passen.</span><span class="sxs-lookup"><span data-stu-id="992be-334">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="992be-335">Bewerkingen van een functie retour neren</span><span class="sxs-lookup"><span data-stu-id="992be-335">Returning operations from a function</span></span>

<span data-ttu-id="992be-336">We zijn van belang dat we ook bewerkingen kunnen retour neren als onderdeel van de uitvoer, zodat we bepaalde soorten klassieke voorwaardelijke logica kunnen isoleren als een klassieke functie waarmee een beschrijving van een Quantum programma wordt geretourneerd in de vorm van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-336">We emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="992be-337">Als eenvoudig voor beeld kunt u het voor beeld van teleportie overwegen, waarbij de partij die een twee-bits klassiek bericht ontvangt, het bericht moet gebruiken om hun Qubit te decoderen naar de juiste teleportal-status.</span><span class="sxs-lookup"><span data-stu-id="992be-337">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="992be-338">We kunnen dit schrijven in termen van een functie die deze twee klassieke bits accepteert en de juiste decodeer bewerking retourneert.</span><span class="sxs-lookup"><span data-stu-id="992be-338">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

<span data-ttu-id="992be-339">Deze nieuwe functie is inderdaad een functie, in dat geval als we deze aanroepen met dezelfde waarden van `hereBit` en `thereBit` , zullen we altijd dezelfde bewerking ophalen.</span><span class="sxs-lookup"><span data-stu-id="992be-339">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="992be-340">Het is dus mogelijk dat de decoder veilig kan worden uitgevoerd binnen bewerkingen zonder dat dit de reden hoeft te zijn van de manier waarop de decodeer logica communiceert met de definities van de verschillende bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="992be-340">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="992be-341">Dat wil zeggen dat we de klassieke logica binnen een functie hebben geïsoleerd, zodat de compiler kan worden gevolgd met impunity, zolang de invoer wordt bewaard.</span><span class="sxs-lookup"><span data-stu-id="992be-341">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="992be-342">Gedeeltelijke toepassing</span><span class="sxs-lookup"><span data-stu-id="992be-342">Partial Application</span></span>

<span data-ttu-id="992be-343">We kunnen aanzienlijk meer doen met functies die bewerkingen retour neren met behulp van *gedeeltelijke toepassing*, waarbij we een of meer delen van de invoer kunnen bieden aan een functie of bewerking zonder dat deze daad werkelijk wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="992be-343">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="992be-344">`ApplyTwice`Als u bijvoorbeeld het bovenstaande voor beeld aanroept, kunt u aangeven dat we niet meteen willen opgeven, op welke Qubit de invoer bewerking moet worden toegepast:</span><span class="sxs-lookup"><span data-stu-id="992be-344">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="992be-345">In dit geval bevat de lokale variabele `twiceOp` de gedeeltelijk toegepaste bewerking `ApplyTwice(op, _)` , waarbij delen van de invoer die nog niet zijn opgegeven, worden aangegeven door `_` .</span><span class="sxs-lookup"><span data-stu-id="992be-345">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="992be-346">Wanneer we de volgende regel daad werkelijk aanroepen `twiceOp` , geven we de invoer door aan de gedeeltelijk toegepaste bewerking van alle resterende delen van de invoer voor de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="992be-346">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="992be-347">Het bovenstaande code fragment is dus in feite identiek aan het `ApplyTwice(op, target)` rechtstreeks aanroepen van, opslaan voor dat we een nieuwe lokale variabele hebben geïntroduceerd waarmee we de oproep kunnen vertragen tijdens het leveren van bepaalde onderdelen van de invoer.</span><span class="sxs-lookup"><span data-stu-id="992be-347">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="992be-348">Omdat een bewerking die gedeeltelijk is toegepast, niet daad werkelijk wordt aangeroepen totdat de volledige invoer is opgegeven, kunnen we bewerkingen gedeeltelijk Toep assen, zelfs binnen functies.</span><span class="sxs-lookup"><span data-stu-id="992be-348">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="992be-349">In principe is de klassieke logica binnen `SquareOperation` mogelijk veel meer betrokken, maar is deze nog steeds geïsoleerd van de rest van een bewerking door de garanties dat de compiler over functies kan bieden.</span><span class="sxs-lookup"><span data-stu-id="992be-349">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="992be-350">Deze benadering wordt gebruikt in de standaard bibliotheek van Q # voor het uitdrukken van de klassieke controle stroom op een manier die eenvoudig kan worden gebruikt binnen Quantum Program ma's.</span><span class="sxs-lookup"><span data-stu-id="992be-350">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>


## <a name="recursion"></a><span data-ttu-id="992be-351">Recursie</span><span class="sxs-lookup"><span data-stu-id="992be-351">Recursion</span></span>

<span data-ttu-id="992be-352">Q # callables mogen direct of indirect recursief zijn.</span><span class="sxs-lookup"><span data-stu-id="992be-352">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="992be-353">Dat wil zeggen dat een bewerking of functie zichzelf kan aanroepen, of een andere aanroep kan aanroepen die direct of indirect de aanroep bare bewerking aanroept.</span><span class="sxs-lookup"><span data-stu-id="992be-353">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="992be-354">Er zijn twee belang rijke opmerkingen over het gebruik van recursie, echter:</span><span class="sxs-lookup"><span data-stu-id="992be-354">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="992be-355">Het gebruik van recursie in bewerkingen heeft waarschijnlijk een conflict met bepaalde optimalisaties.</span><span class="sxs-lookup"><span data-stu-id="992be-355">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="992be-356">Dit kan een aanzienlijke invloed hebben op de uitvoerings tijd van de algoritme.</span><span class="sxs-lookup"><span data-stu-id="992be-356">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="992be-357">Bij het uitvoeren van een echt Quantum apparaat kan de stack-ruimte beperkt zijn en kan een grondige recursie leiden tot een runtime-fout.</span><span class="sxs-lookup"><span data-stu-id="992be-357">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="992be-358">Met name de Q #-compiler en runtime identificeren en optimaliseren de staart recursie niet.</span><span class="sxs-lookup"><span data-stu-id="992be-358">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="next-steps"></a><span data-ttu-id="992be-359">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="992be-359">Next steps</span></span>

<span data-ttu-id="992be-360">Meer informatie over [variabelen](xref:microsoft.quantum.guide.variables) in Q #.</span><span class="sxs-lookup"><span data-stu-id="992be-360">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>