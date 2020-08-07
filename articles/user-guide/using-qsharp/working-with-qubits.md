---
title: Werken met qubits
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6808a852ee0de7d3a38ea44e9637eeaa6bea382a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867859"
---
# <a name="working-with-qubits"></a><span data-ttu-id="9ae50-103">Werken met qubits</span><span class="sxs-lookup"><span data-stu-id="9ae50-103">Working with qubits</span></span>

<span data-ttu-id="9ae50-104">Qubits zijn het fundamenteel object van informatie in Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="9ae50-104">Qubits are the fundamental object of information in quantum computing.</span></span> <span data-ttu-id="9ae50-105">Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor een algemene inleiding tot qubits [over Quantum Computing](xref:microsoft.quantum.overview.understanding), en voor meer informatie over de wiskundige weer gave ervan.</span><span class="sxs-lookup"><span data-stu-id="9ae50-105">For a general introduction to qubits, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), and to dive deeper into their mathematical representation, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span> 

<span data-ttu-id="9ae50-106">In dit artikel wordt beschreven hoe u met qubits in een programma kunt werken Q# .</span><span class="sxs-lookup"><span data-stu-id="9ae50-106">This article explores how to use and work with qubits in a Q# program.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="9ae50-107">Geen van de instructies die in dit artikel worden besproken, is geldig in de hoofd tekst van een functie.</span><span class="sxs-lookup"><span data-stu-id="9ae50-107">None of the statements discussed in this article are valid within the body of a function.</span></span> <span data-ttu-id="9ae50-108">Ze zijn alleen geldig in-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="9ae50-108">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="9ae50-109">Qubits toewijzen</span><span class="sxs-lookup"><span data-stu-id="9ae50-109">Allocating Qubits</span></span>

<span data-ttu-id="9ae50-110">Omdat fysieke qubits een kostbaar middel zijn in een quantum computer, moet u een deel van de taak van de compiler controleren om ervoor te zorgen dat ze zo efficiënt mogelijk worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9ae50-110">Because physical qubits are a precious resource in a quantum computer, part of the compiler's job is to make sure they are being used as efficiently as possible.</span></span>
<span data-ttu-id="9ae50-111">Als zodanig moet u aangeven dat u Q# qubits wilt *toewijzen* voor gebruik binnen een bepaald instructie blok.</span><span class="sxs-lookup"><span data-stu-id="9ae50-111">As such, you need to tell Q# to *allocate* qubits for use within a particular statement block.</span></span>
<span data-ttu-id="9ae50-112">U kunt qubits toewijzen als één Qubit, of als een matrix van qubits, ook wel een *REGI ster*genoemd.</span><span class="sxs-lookup"><span data-stu-id="9ae50-112">You can allocate qubits as a single qubit, or as an array of qubits, known as a *register*.</span></span> 

### <a name="clean-qubits"></a><span data-ttu-id="9ae50-113">Qubits opschonen</span><span class="sxs-lookup"><span data-stu-id="9ae50-113">Clean qubits</span></span>

<span data-ttu-id="9ae50-114">Gebruik de `using` instructie om nieuwe qubits toe te wijzen voor gebruik tijdens een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="9ae50-114">Use the `using` statement to allocate new qubits for use during a statement block.</span></span>

<span data-ttu-id="9ae50-115">De instructie bestaat uit het tref woord `using` , gevolgd door een binding tussen haakjes `( )` en het instructie blok waarbinnen de qubits beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="9ae50-115">The statement consists of the keyword `using`, followed by a binding enclosed in parentheses `( )` and the statement block within which the qubits are available.</span></span>
<span data-ttu-id="9ae50-116">De binding volgt hetzelfde patroon als `let` instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=` en een enkele waarde of een overeenkomende tuple van *initializers*.</span><span class="sxs-lookup"><span data-stu-id="9ae50-116">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="9ae50-117">Initialisatie functies zijn beschikbaar voor één Qubit, aangeduid als `Qubit()` , of een matrix van qubits, `Qubit[n]` , waarbij `n` een `Int` expressie is.</span><span class="sxs-lookup"><span data-stu-id="9ae50-117">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="9ae50-118">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="9ae50-118">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="9ae50-119">Alle qubits die op deze manier zijn toegewezen, worden met de {0} status $ \ket $ gestart.</span><span class="sxs-lookup"><span data-stu-id="9ae50-119">Any qubits allocated in this way start off in the $\ket{0}$ state.</span></span> <span data-ttu-id="9ae50-120">In het vorige voor beeld `auxiliary` is een enkelvoudige Qubit in de status $ \ket {0} $ en `register` bevindt zich in de vijf Qubit-status $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="9ae50-120">Thus in the previous example, `auxiliary` is a single qubit in the state $\ket{0}$, and `register` is in the five-qubit state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="9ae50-121">Aan het einde van het `using` blok worden alle qubits die zijn toegewezen door dat blok onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9ae50-121">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="9ae50-122">Doel machines kunnen ontoegewezen qubits opnieuw gebruiken en deze aanbieden aan andere `using` blokken voor toewijzing.</span><span class="sxs-lookup"><span data-stu-id="9ae50-122">Target machines can reuse deallocated qubits and offer them to other `using` blocks for allocation.</span></span> <span data-ttu-id="9ae50-123">Als zodanig verwacht de doel computer dat qubits zich in de $ \ket $-status bevindt onmiddellijk voordat de toewijzing wordt opgeheven {0} .</span><span class="sxs-lookup"><span data-stu-id="9ae50-123">As such, the target machine expects that qubits are in the $\ket{0}$ state immediately before deallocation.</span></span>
> <span data-ttu-id="9ae50-124">Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="9ae50-124">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="9ae50-125">Als dat het geval is, kunt u de @"microsoft.quantum.intrinsic.reset" bewerking, die de Qubit retourneert naar $ \ket $, gebruiken {0} door deze te meten en voorwaardelijk een bewerking uit te voeren op basis van het resultaat.</span><span class="sxs-lookup"><span data-stu-id="9ae50-125">If need be, you can use the @"microsoft.quantum.intrinsic.reset" operation, which returns the qubit to $\ket{0}$ by measuring it and conditionally performing an operation based on the result.</span></span> <span data-ttu-id="9ae50-126">Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.</span><span class="sxs-lookup"><span data-stu-id="9ae50-126">Such a measurement destroys any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="9ae50-127">Geleed qubits</span><span class="sxs-lookup"><span data-stu-id="9ae50-127">Borrowed Qubits</span></span>

<span data-ttu-id="9ae50-128">Gebruik de `borrowing` instructie om qubits toe te wijzen voor tijdelijk gebruik, die geen specifieke status hoeven te hebben.</span><span class="sxs-lookup"><span data-stu-id="9ae50-128">Use the `borrowing` statement to allocate qubits for temporary use, which do not need to be in a specific state.</span></span>

<span data-ttu-id="9ae50-129">U kunt gelede qubits als Scratch ruimte gebruiken tijdens een berekening.</span><span class="sxs-lookup"><span data-stu-id="9ae50-129">You can use borrowed qubits as scratch space during a computation.</span></span>
<span data-ttu-id="9ae50-130">Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="9ae50-130">These qubits are generally not in a clean state, that is, they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="9ae50-131">Deze worden vaak aangeduid als ' Dirty ' qubits omdat hun status onbekend is en zelfs kan worden Entangled met andere delen van het geheugen van de quantum computer.</span><span class="sxs-lookup"><span data-stu-id="9ae50-131">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="9ae50-132">De binding volgt hetzelfde patroon en regels als de- `using` instructie.</span><span class="sxs-lookup"><span data-stu-id="9ae50-132">The binding follows the same pattern and rules as the `using` statement.</span></span>
<span data-ttu-id="9ae50-133">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="9ae50-133">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="9ae50-134">De geleende qubits bevinden zich in een onbekende status en het vervalt buiten het bereik aan het einde van het instructie blok.</span><span class="sxs-lookup"><span data-stu-id="9ae50-134">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="9ae50-135">De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden bij het lenen daarvan; dat wil zeggen dat de status aan het begin en het einde van het instructie blok hetzelfde moet zijn.</span><span class="sxs-lookup"><span data-stu-id="9ae50-135">The borrower commits to leaving the qubits in the same state they were in when they borrowed them; that is, their state at the beginning and the end of the statement block should be the same.</span></span>
<span data-ttu-id="9ae50-136">Omdat deze status niet noodzakelijkerwijs een klassieke status is, mogen in de meeste gevallen het lenen van scopes geen metingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="9ae50-136">Because this state is not necessarily a classical state, in most cases borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="9ae50-137">Bij het lenen van qubits probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend in de hoofd tekst van de `borrowing` instructie.</span><span class="sxs-lookup"><span data-stu-id="9ae50-137">When borrowing qubits, the system first tries to fill the request from qubits that are in use but not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="9ae50-138">Als er onvoldoende qubits zijn, wijst deze nieuwe qubits toe om de aanvraag te volt ooien.</span><span class="sxs-lookup"><span data-stu-id="9ae50-138">If there aren't enough such qubits, then it allocates new qubits to complete the request.</span></span>

<span data-ttu-id="9ae50-139">In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.</span><span class="sxs-lookup"><span data-stu-id="9ae50-139">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="9ae50-140">Zie voor een voor beeld van het gebruik in Q# het [lenen van qubits-voor beeld](#borrowing-qubits-example) in dit artikel of het papier [*confactoring met 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een algoritme die gebruikmaakt van geleed qubits.</span><span class="sxs-lookup"><span data-stu-id="9ae50-140">For an example of their use in Q#, see [Borrowing Qubits Example](#borrowing-qubits-example) in this article, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="9ae50-141">Intrinsieke bewerkingen</span><span class="sxs-lookup"><span data-stu-id="9ae50-141">Intrinsic Operations</span></span>

<span data-ttu-id="9ae50-142">Zodra de toewijzing is toegewezen, kunt u een Qubit door geven aan functies en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="9ae50-142">Once allocated, you can pass a qubit to functions and operations.</span></span>
<span data-ttu-id="9ae50-143">In sommige zin is dit alles wat een Q# programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="9ae50-143">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>

<span data-ttu-id="9ae50-144">In dit artikel worden enkele nuttige Q# bewerkingen besproken die u kunt gebruiken om te communiceren met qubits.</span><span class="sxs-lookup"><span data-stu-id="9ae50-144">This article discusses a few useful Q# operations that you can use to interact with qubits.</span></span>
<span data-ttu-id="9ae50-145">Zie [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude)voor meer informatie over deze en andere.</span><span class="sxs-lookup"><span data-stu-id="9ae50-145">For more detail about these and others, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span> 

<span data-ttu-id="9ae50-146">Eerst worden de Pauli-Opera tors (single-Qubit) $X $, $Y $ en $Z $ weer gegeven in Q# de intrinsieke bewerkingen [`X`](xref:microsoft.quantum.intrinsic.x) , [`Y`](xref:microsoft.quantum.intrinsic.y) en [`Z`](xref:microsoft.quantum.intrinsic.z) die elk type hebben `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-146">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations [`X`](xref:microsoft.quantum.intrinsic.x), [`Y`](xref:microsoft.quantum.intrinsic.y), and [`Z`](xref:microsoft.quantum.intrinsic.z), each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="9ae50-147">Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), beschouw $X $ en dus `X` als een bits-Flip-bewerking of niet-poort.</span><span class="sxs-lookup"><span data-stu-id="9ae50-147">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="9ae50-148">U kunt de `X` bewerking voor het voorbereiden van statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een klassieke-bits teken reeks $s $:</span><span class="sxs-lookup"><span data-stu-id="9ae50-148">You can use the `X` operation to prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="9ae50-149">Later ziet u een compactere manier om deze bewerking te schrijven waarvoor geen hand matige controle stroom is vereist.</span><span class="sxs-lookup"><span data-stu-id="9ae50-149">Later, you will see more compact ways of writing this operation that do not require manual control flow.</span></span>

<span data-ttu-id="9ae50-150">U kunt ook statussen voorbereiden zoals $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ en $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ met behulp van de Hadamard Transform $H $, die wordt vertegenwoordigd Q# door de intrinsieke bewerking [`H`](xref:microsoft.quantum.intrinsic.h) (ook type (Qubit => eenheid is ADJ en CTL)):</span><span class="sxs-lookup"><span data-stu-id="9ae50-150">You can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation [`H`](xref:microsoft.quantum.intrinsic.h) (also of type (Qubit => Unit is Adj + Ctl)\`):</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="9ae50-151">Metingen</span><span class="sxs-lookup"><span data-stu-id="9ae50-151">Measurements</span></span>

<span data-ttu-id="9ae50-152">Metingen van afzonderlijke qubits kunnen worden uitgevoerd in verschillende slagen, die allemaal vertegenwoordigd worden door een Paulias op de [Bloch-bol](xref:microsoft.quantum.glossary#bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="9ae50-152">Measurements of individual qubits can be performed in different bases, each represented by a Pauli axis on the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span></span>
<span data-ttu-id="9ae50-153">De *reken kundige basis* verwijst naar de `PauliZ` basis en is de meest voorkomende basis voor de meting.</span><span class="sxs-lookup"><span data-stu-id="9ae50-153">The *computational basis* refers to the `PauliZ` basis, and is the most common basis used for measurement.</span></span>

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a><span data-ttu-id="9ae50-154">Eén Qubit meten op `PauliZ` basis</span><span class="sxs-lookup"><span data-stu-id="9ae50-154">Measure a single qubit in the `PauliZ` basis</span></span>

<span data-ttu-id="9ae50-155">Gebruik de [`M`](xref:microsoft.quantum.intrinsic.m) bewerking, een ingebouwde, intrinsieke, niet-unitary bewerking, om één Qubit te meten op `PauliZ` basis en een klassieke waarde aan het resultaat toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="9ae50-155">Use the [`M`](xref:microsoft.quantum.intrinsic.m) operation, which is a built-in intrinsic non-unitary operation, to measure a single qubit in the `PauliZ` basis and assign a classical value to the result.</span></span>
<span data-ttu-id="9ae50-156">`M`heeft een gereserveerd retour type, `Result` dat alleen waarden kan overnemen `Zero` of `One` overeenkomt met de gemeten statussen $ \ket {0} $ of $ \ket {1} $-geeft aan dat het resultaat geen Quantum status meer is.</span><span class="sxs-lookup"><span data-stu-id="9ae50-156">`M` has a reserved return type, `Result`, which can only take values `Zero` or `One` corresponding to the measured states $\ket{0}$ or $\ket{1}$ - indicating that the result is no longer a quantum state.</span></span>

<span data-ttu-id="9ae50-157">Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket {0} $-status, vervolgens een Hadamard-bewerking toepast `H` op de waarde en het resultaat op basis daarvan meet `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-157">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a><span data-ttu-id="9ae50-158">Een of meer qubits meten in specifieke bases</span><span class="sxs-lookup"><span data-stu-id="9ae50-158">Measure one or more qubits in specific bases</span></span>

<span data-ttu-id="9ae50-159">U kunt de bewerking gebruiken om een matrix van een of meer qubits in een specifieke Base te meten [`Measure`](xref:microsoft.quantum.intrinsic.measure) .</span><span class="sxs-lookup"><span data-stu-id="9ae50-159">To measure an array of one or more qubits in specific bases, you can use the [`Measure`](xref:microsoft.quantum.intrinsic.measure) operation.</span></span>

<span data-ttu-id="9ae50-160">De invoer voor `Measure` is een matrix van `Pauli` typen (bijvoorbeeld `[PauliX, PauliZ, PauliZ]` ) en een matrix van qubits.</span><span class="sxs-lookup"><span data-stu-id="9ae50-160">The inputs to `Measure` are an array of `Pauli` types (for example, `[PauliX, PauliZ, PauliZ]`) and an array of qubits.</span></span>

<span data-ttu-id="9ae50-161">Een iets ingewik kelder voor beeld wordt gegeven door de volgende bewerking, waarmee de Boole-waarde wordt geretourneerd `true` als alle qubits in een REGI ster van `Qubit[]` het type in de status nul staan wanneer deze worden gemeten in een opgegeven Pauli, en die `false` anders retourneert.</span><span class="sxs-lookup"><span data-stu-id="9ae50-161">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="9ae50-162">Houd er rekening mee dat in dit voor beeld nog steeds alleen `Measure` een afzonderlijke qubits wordt uitgevoerd, maar de bewerking kan worden uitgebreid naar gezamenlijke metingen op meerdere qubits.</span><span class="sxs-lookup"><span data-stu-id="9ae50-162">Note that this example still only performs `Measure` on individual qubits one at a time, but the operation can be extended to joint measurements on multiple qubits.</span></span>

## <a name="borrowing-qubits-example"></a><span data-ttu-id="9ae50-163">Lenen van qubits-voor beeld</span><span class="sxs-lookup"><span data-stu-id="9ae50-163">Borrowing Qubits Example</span></span>

<span data-ttu-id="9ae50-164">Er zijn voor beelden in de Canon die gebruikmaken van het `borrowing` tref woord, zoals de volgende functie `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-164">There are examples in the canon that use the `borrowing` keyword, such as the following function `MultiControlledXBorrow`.</span></span> <span data-ttu-id="9ae50-165">Als u `controls` het besturings element qubits dat aan een bewerking moet worden toegevoegd `X` , wordt het aantal Dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) toegevoegd door deze implementatie `Length(controls)-2` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-165">If `controls` denotes the control qubits to add to an `X` operation, then the number of dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) added by this implementation is `Length(controls)-2`.</span></span>

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

<span data-ttu-id="9ae50-166">In dit voor beeld is een uitgebreid gebruik van de `With` Combinator gebruikt, in het formulier dat van toepassing is op bewerkingen die adjoint ondersteunen, bijvoorbeeld `WithA` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-166">Note that this example used extensive use of the `With` combinator, in its form that is applicable for operations that support adjoint, for example, `WithA`.</span></span>
<span data-ttu-id="9ae50-167">Dit is een goede programmeer stijl, omdat het besturings element wordt toegevoegd aan structuren waarbij `With` alleen de interne bewerking wordt door gegeven aan de besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="9ae50-167">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="9ae50-168">Houd er ook rekening mee dat naast de `body` bewerking een implementatie van de `controlled` hoofd tekst van de bewerking expliciet is gegeven, in plaats van een instructie te gebruiken `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-168">Also note that, in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="9ae50-169">De reden hiervoor is dat, vanwege de structuur van het circuit, het eenvoudig is om verdere besturings elementen toe te voegen, wat nuttig is ten opzichte van het toevoegen van controle aan elke poort in de `body` .</span><span class="sxs-lookup"><span data-stu-id="9ae50-169">The reason for this is that, because of the structure of the circuit, it is easy to add further controls, which is beneficial compared to adding control to each gate in the `body`.</span></span> 

<span data-ttu-id="9ae50-170">Het is een goed proces om deze code te vergelijken met een andere Canon `MultiControlledXClean` -functie die hetzelfde doel heeft voor het implementeren van een `X` door een besturings systeem beheerde bewerking, maar die gebruikmaakt van verschillende schone qubits met behulp van het `using` mechanisme.</span><span class="sxs-lookup"><span data-stu-id="9ae50-170">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="9ae50-171">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="9ae50-171">Next steps</span></span>

<span data-ttu-id="9ae50-172">Meer informatie over [controle stroom](xref:microsoft.quantum.guide.controlflow) in Q# .</span><span class="sxs-lookup"><span data-stu-id="9ae50-172">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>