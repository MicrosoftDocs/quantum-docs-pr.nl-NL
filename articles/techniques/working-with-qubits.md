---
title: Werken met qubits
description: 'Werken met qubits-Q #-technieken'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: dc6db93dadc37534aece9624fe516125d919f8cd
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819991"
---
# <a name="working-with-qubits"></a><span data-ttu-id="57f77-103">Werken met qubits</span><span class="sxs-lookup"><span data-stu-id="57f77-103">Working with Qubits</span></span>

<span data-ttu-id="57f77-104">Als u nu een aantal verschillende onderdelen van de Q #-taal hebt gezien, laat u ons daar het dik van zien en ziet u hoe u qubits zelf kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="57f77-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="57f77-105">Qubits toewijzen</span><span class="sxs-lookup"><span data-stu-id="57f77-105">Allocating Qubits</span></span>

<span data-ttu-id="57f77-106">Voor het verkrijgen van een Qubit die we in Q # kunnen gebruiken, wijzen we qubits binnen een `using`-blok *toe* :</span><span class="sxs-lookup"><span data-stu-id="57f77-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="57f77-107">Alle qubits die op deze manier zijn toegewezen, worden gestart in de $ \ket{0}$-status; in het bovenstaande voor beeld is `register` dus de status $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="57f77-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="57f77-108">Aan het einde van het `using` blok worden alle qubits die door dat blok zijn toegewezen, onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="57f77-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="57f77-109">Doel computers verwachten dat qubits zich in $ \ket{0}$ staat onmiddellijk voordat de toewijzing ongedaan wordt gemaakt, zodat ze opnieuw kunnen worden gebruikt en worden aangeboden aan andere `using` blokken voor toewijzing.</span><span class="sxs-lookup"><span data-stu-id="57f77-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="57f77-110">Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="57f77-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="57f77-111">Als dat het geval is, kan de @"microsoft.quantum.intrinsic.reset" bewerking worden gebruikt om in plaats daarvan een Qubit te meten en dit meet resultaat te gebruiken om ervoor te zorgen dat de gemeten Qubit wordt geretourneerd naar $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="57f77-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="57f77-112">Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.</span><span class="sxs-lookup"><span data-stu-id="57f77-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="57f77-113">Intrinsieke bewerkingen</span><span class="sxs-lookup"><span data-stu-id="57f77-113">Intrinsic Operations</span></span>

<span data-ttu-id="57f77-114">Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan functies en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="57f77-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="57f77-115">In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="57f77-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="57f77-116">Deze bewerkingen worden in meer detail weer gegeven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), maar we noemen nu enkele nuttige bewerkingen die kunnen worden gebruikt om te communiceren met qubits.</span><span class="sxs-lookup"><span data-stu-id="57f77-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="57f77-117">Eerst worden de Pauli-Opera tors met één Qubit $X $, $Y $ en $Z $ weer gegeven in Q # door de intrinsieke bewerkingen `X`, `Y`en `Z`, die elk het type `(Qubit => Unit is Adj + Ctl)`hebben.</span><span class="sxs-lookup"><span data-stu-id="57f77-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="57f77-118">Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), kunnen we $X $ en dus `X` als een bits-Flip-bewerking of niet-poort.</span><span class="sxs-lookup"><span data-stu-id="57f77-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="57f77-119">Met de `X` bewerking kunnen wij statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een bepaalde klassieke-bits teken reeks $s $ voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="57f77-119">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="57f77-120">Later worden er meer compacte manieren weer gegeven voor het schrijven van deze bewerking waarvoor hand matige Datatransport besturing niet is vereist.</span><span class="sxs-lookup"><span data-stu-id="57f77-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="57f77-121">We kunnen ook staten voorbereiden zoals $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ en $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ door gebruik te maken van de Hadamard Transform $H $, die wordt weer gegeven in Q # door de intrinsieke bewerking `H : (Qubit => Unit is Adj + Ctl)`:</span><span class="sxs-lookup"><span data-stu-id="57f77-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="57f77-122">Metingen</span><span class="sxs-lookup"><span data-stu-id="57f77-122">Measurements</span></span>

<span data-ttu-id="57f77-123">Met behulp van de `Measure` bewerking, een ingebouwde, intrinsieke, niet-unitary bewerking kunnen we klassieke informatie uit een object van het type `Qubit` ophalen en een klassieke waarde als resultaat toewijzen, die een gereserveerd type heeft `Result`, waarmee wordt aangegeven dat het resultaat geen Quantum status meer is.</span><span class="sxs-lookup"><span data-stu-id="57f77-123">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="57f77-124">De invoer voor `Measure` is een Pauli-as op de Bloch-bol, vertegenwoordigd door een waarde van het type `Pauli` (voor instantie `PauliX`) en een waarde van het type `Qubit`.</span><span class="sxs-lookup"><span data-stu-id="57f77-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="57f77-125">Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket{0}$-status, waarna een Hadamard-bewerking `H` wordt toegepast en het resultaat wordt gemeten in de `PauliZ` basis.</span><span class="sxs-lookup"><span data-stu-id="57f77-125">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="57f77-126">Een iets ingewik kelder voor beeld wordt gegeven door de volgende bewerking, waarmee de Booleaanse waarde wordt geretourneerd `true` als alle qubits in een REGI ster van het type `Qubit[]` de status nul hebben wanneer ze worden gemeten in een opgegeven Pauli, en die `false` anders retourneert.</span><span class="sxs-lookup"><span data-stu-id="57f77-126">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="57f77-127">De Q #-taal staat de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.</span><span class="sxs-lookup"><span data-stu-id="57f77-127">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="57f77-128">Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="57f77-128">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="57f77-129">Een voor beeld is het eenvoudig om te implementeren, dat wil zeggen, *herhalen-tot-succes-* patronen (RUS) in Q #.</span><span class="sxs-lookup"><span data-stu-id="57f77-129">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="57f77-130">Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben, maar waarvoor de werkelijke kosten afhankelijk zijn van een feitelijke uitvoering en een daad werkelijke interleaving van verschillende mogelijke vertakkingen.</span><span class="sxs-lookup"><span data-stu-id="57f77-130">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="57f77-131">Q # ondersteunt de construct om herhaalde tot geslaagd (RUS) patronen te vergemakkelijken.</span><span class="sxs-lookup"><span data-stu-id="57f77-131">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

<span data-ttu-id="57f77-132">waar `statementBlock1` en `statementBlock2` geen of meer Q #-instructies zijn, en `expression` een geldige expressie die resulteert in een waarde van het type `Bool`.</span><span class="sxs-lookup"><span data-stu-id="57f77-132">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="57f77-133">In een typische use-case implementeert de volgende Q #-bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt{5}$ op de Bloch-bol.</span><span class="sxs-lookup"><span data-stu-id="57f77-133">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="57f77-134">Dit wordt bereikt door gebruik te maken van een bekend RUS-patroon:</span><span class="sxs-lookup"><span data-stu-id="57f77-134">This is accomplished by using a known RUS pattern:</span></span>

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

<span data-ttu-id="57f77-135">In dit voor beeld ziet u het gebruik van een onveranderlijke variabele `finished` die binnen het bereik van de volledige herhalings-tot-reparatie-lus ligt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.</span><span class="sxs-lookup"><span data-stu-id="57f77-135">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="57f77-136">Tot slot wordt een voor beeld van een RUS-patroon weer gegeven om een Quantum status te bereiden $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, te beginnen bij de status $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="57f77-136">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="57f77-137">Zie ook het [voor beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="57f77-137">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
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

<span data-ttu-id="57f77-138">Opvallende programmatische functies die in deze bewerking worden weer gegeven, zijn een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen worden betrokken, en het gebruik van `AssertProb`-instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="57f77-138">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="57f77-139">Zie ook [testen en fout opsporing](xref:microsoft.quantum.techniques.testing-and-debugging) voor meer informatie over de [`Assert`](xref:microsoft.quantum.intrinsic.assert) en [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="57f77-139">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>
