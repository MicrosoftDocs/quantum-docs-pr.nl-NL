---
title: Werken met qubits
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: e89b9ccfe2a0796e01eedfc99f7ce71038d85f38
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430931"
---
# <a name="working-with-qubits"></a><span data-ttu-id="41703-103">Werken met qubits</span><span class="sxs-lookup"><span data-stu-id="41703-103">Working with qubits</span></span>

<span data-ttu-id="41703-104">Als u nu een aantal verschillende onderdelen van de Q #-taal hebt gezien, laat u ons daar het dik van zien en ziet u hoe u qubits zelf kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="41703-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

<span data-ttu-id="41703-105">Houd er rekening mee dat geen van deze instructies zijn toegestaan in de hoofd tekst van een functie.</span><span class="sxs-lookup"><span data-stu-id="41703-105">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="41703-106">Ze zijn alleen geldig in-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="41703-106">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="41703-107">Qubits toewijzen</span><span class="sxs-lookup"><span data-stu-id="41703-107">Allocating Qubits</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="41703-108">Qubits opschonen</span><span class="sxs-lookup"><span data-stu-id="41703-108">Clean qubits</span></span>

<span data-ttu-id="41703-109">De `using` instructie wordt gebruikt om nieuwe qubits *toe te wijzen* voor gebruik tijdens een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="41703-109">The `using` statement is used to *allocate* new qubits for use during a statement block.</span></span>

<span data-ttu-id="41703-110">De instructie bestaat uit het tref woord `using` , gevolgd door een haakje openen, `(` een binding, een haakje sluiten `)` en het instructie blok waarbinnen de qubits beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="41703-110">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="41703-111">De binding volgt hetzelfde patroon als `let` instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=` en een enkele waarde of een overeenkomende tuple van *initializers*.</span><span class="sxs-lookup"><span data-stu-id="41703-111">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="41703-112">Initialisatie functies zijn beschikbaar voor één Qubit, aangeduid als `Qubit()` , of een matrix van qubits, `Qubit[n]` , waarbij `n` een `Int` expressie is.</span><span class="sxs-lookup"><span data-stu-id="41703-112">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="41703-113">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="41703-113">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="41703-114">Alle qubits die op deze manier zijn toegewezen, worden in de $ \ket {0} $-status in het bovenstaande voor beeld gestart met `register` de status $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="41703-114">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="41703-115">Aan het einde van het `using` blok worden alle qubits die zijn toegewezen door dat blok onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41703-115">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="41703-116">Doel computers verwachten dat qubits zich direct vóór de toewijzing van de $ \ket $ bevindt {0} , zodat ze opnieuw kunnen worden gebruikt en voor toewijzing aan andere blokken worden aangeboden `using` .</span><span class="sxs-lookup"><span data-stu-id="41703-116">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="41703-117">Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="41703-117">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="41703-118">Als dat het geval @"microsoft.quantum.intrinsic.reset" is, kan de bewerking worden gebruikt om in plaats daarvan een Qubit te meten en dit meet resultaat te gebruiken om ervoor te zorgen dat de gemeten Qubit wordt geretourneerd naar $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="41703-118">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="41703-119">Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.</span><span class="sxs-lookup"><span data-stu-id="41703-119">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="41703-120">Geleed qubits</span><span class="sxs-lookup"><span data-stu-id="41703-120">Borrowed Qubits</span></span>

<span data-ttu-id="41703-121">De `borrowing` instructie wordt gebruikt om qubits beschikbaar te maken voor tijdelijk gebruik, die geen specifieke status hebben.</span><span class="sxs-lookup"><span data-stu-id="41703-121">The `borrowing` statement is used to make qubits available for temporary use, which do not need be in a specific state.</span></span>

<span data-ttu-id="41703-122">Met het lenende mechanisme kunt u de toewijzing van qubits die als Scratch ruimte kan worden gebruikt tijdens een berekening.</span><span class="sxs-lookup"><span data-stu-id="41703-122">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span>
<span data-ttu-id="41703-123">Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="41703-123">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="41703-124">Deze worden vaak aangeduid als ' Dirty ' qubits omdat hun status onbekend is en zelfs kan worden Entangled met andere delen van het geheugen van de quantum computer.</span><span class="sxs-lookup"><span data-stu-id="41703-124">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="41703-125">De binding volgt hetzelfde patroon en dezelfde regels als in een- `using` instructie.</span><span class="sxs-lookup"><span data-stu-id="41703-125">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>
<span data-ttu-id="41703-126">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="41703-126">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="41703-127">De geleende qubits bevinden zich in een onbekende status en het vervalt buiten het bereik aan het einde van het instructie blok.</span><span class="sxs-lookup"><span data-stu-id="41703-127">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="41703-128">De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden toen ze werden uitgeleend, d.w.z. hun status aan het begin en aan het einde van het blok van de verklaring, wordt naar verwachting hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="41703-128">The borrower commits to leaving the qubits in the same state they were in when they were borrowed,  i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="41703-129">Deze status is in het bijzonder niet noodzakelijkerwijs een klassieke staat, zoals in de meeste gevallen, het lenen van scopes mag geen metingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="41703-129">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="41703-130">Wanneer qubits wordt uitgeleend, probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend tijdens de hoofd tekst van de `borrowing` instructie.</span><span class="sxs-lookup"><span data-stu-id="41703-130">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="41703-131">Als er onvoldoende qubits zijn, wordt er nieuwe qubits toegewezen om de aanvraag te volt ooien.</span><span class="sxs-lookup"><span data-stu-id="41703-131">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>


<span data-ttu-id="41703-132">In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.</span><span class="sxs-lookup"><span data-stu-id="41703-132">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="41703-133">Zie het [qubits-voor beeld](#borrowing-qubits-example) hieronder om een voor beeld te zien van het gebruik in Q # of de papier [*factor die gebruikmaakt van 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een algoritme die gebruikmaakt van geleed qubits.</span><span class="sxs-lookup"><span data-stu-id="41703-133">See the [Borrowing Qubits Example](#borrowing-qubits-example) below to see an example of their use in Q#, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>


## <a name="intrinsic-operations"></a><span data-ttu-id="41703-134">Intrinsieke bewerkingen</span><span class="sxs-lookup"><span data-stu-id="41703-134">Intrinsic Operations</span></span>

<span data-ttu-id="41703-135">Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan functies en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="41703-135">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="41703-136">In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="41703-136">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="41703-137">Deze bewerkingen worden in meer detail weer gegeven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), maar we noemen nu enkele nuttige bewerkingen die kunnen worden gebruikt om te communiceren met qubits.</span><span class="sxs-lookup"><span data-stu-id="41703-137">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="41703-138">Eerst worden de Pauli-Opera tors met één Qubit $X $, $Y $ en $Z $ weer gegeven in Q # door de intrinsieke bewerkingen `X` , `Y` en `Z` , die elk type hebben `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="41703-138">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="41703-139">Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), kunnen we $X $ en dus `X` als een bits-Flip-bewerking of niet-poort beschouwen.</span><span class="sxs-lookup"><span data-stu-id="41703-139">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="41703-140">`X`Met deze bewerking kunnen wij statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een klassieke-bits teken reeks $s $ voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="41703-140">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="41703-141">Later worden er meer compacte manieren weer gegeven voor het schrijven van deze bewerking waarvoor hand matige Datatransport besturing niet is vereist.</span><span class="sxs-lookup"><span data-stu-id="41703-141">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="41703-142">We kunnen ook staten voorbereiden zoals $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ en $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ door gebruik te maken van de Hadamard Transform $H $, die wordt weer gegeven in Q # door de intrinsieke bewerking `H : (Qubit => Unit is Adj + Ctl)` :</span><span class="sxs-lookup"><span data-stu-id="41703-142">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="41703-143">Metingen</span><span class="sxs-lookup"><span data-stu-id="41703-143">Measurements</span></span>

<span data-ttu-id="41703-144">Door gebruik te maken van de `Measure` bewerking, een ingebouwde intrinsieke, niet-unitary bewerking, kunnen we klassieke informatie uit een object van het type ophalen `Qubit` en een klassieke waarde als resultaat toewijzen, die een gereserveerd type heeft `Result` . Dit geeft aan dat het resultaat geen Quantum status meer is.</span><span class="sxs-lookup"><span data-stu-id="41703-144">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="41703-145">De invoer naar `Measure` is een Pauli-as op de Bloch-bol, vertegenwoordigd door een waarde van het type `Pauli` (bijvoorbeeld ' instance ' `PauliX` ) en een waarde van het type `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="41703-145">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="41703-146">Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket {0} $-status, vervolgens een Hadamard-bewerking toepast `H` op de waarde en het resultaat op basis daarvan meet `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="41703-146">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="41703-147">Een iets ingewik kelder voor beeld wordt gegeven door de volgende bewerking, waarmee de Boole-waarde wordt geretourneerd `true` als alle qubits in een REGI ster van `Qubit[]` het type in de status nul staan wanneer deze worden gemeten in een opgegeven Pauli, en die `false` anders retourneert.</span><span class="sxs-lookup"><span data-stu-id="41703-147">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

## <a name="borrowing-qubits-example"></a><span data-ttu-id="41703-148">Lenen van qubits-voor beeld</span><span class="sxs-lookup"><span data-stu-id="41703-148">Borrowing Qubits Example</span></span>

<span data-ttu-id="41703-149">In de Canon zijn voor beelden die gebruikmaken `borrowing` van het tref woord, bijvoorbeeld de functie die `MultiControlledXBorrow` hieronder is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="41703-149">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="41703-150">Als `controls` u het besturings element qubits dat moet worden toegevoegd aan een `X` bewerking, wordt er een totaal van een `Length(controls)-2` groot aantal gewijzigde ancillas toegevoegd door deze implementatie.</span><span class="sxs-lookup"><span data-stu-id="41703-150">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

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

<span data-ttu-id="41703-151">Houd er rekening mee dat uitgebreid gebruik van de `With` Combinator----in het formulier dat van toepassing is op bewerkingen die adjoint ondersteunen, dat wil zeggen `WithA` ---is gemaakt in dit voor beeld.</span><span class="sxs-lookup"><span data-stu-id="41703-151">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example.</span></span>
<span data-ttu-id="41703-152">Dit is een goede programmeer stijl, omdat het besturings element wordt toegevoegd aan structuren waarbij `With` alleen de interne bewerking wordt door gegeven aan de besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="41703-152">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="41703-153">Daarnaast `body` is de implementatie van de hoofd tekst van de bewerking niet alleen van toepassing op `controlled` een instructie, maar u kunt er ook voor kiezen `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="41703-153">Further, note that here in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="41703-154">De reden hiervoor is dat we van de structuur van het circuit weten hoe u eenvoudig extra besturings elementen kunt toevoegen die nuttig zijn ten opzichte van het toevoegen van controle aan elke afzonderlijke poort in de `body` .</span><span class="sxs-lookup"><span data-stu-id="41703-154">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="41703-155">Het is een goed proces om deze code te vergelijken met een andere Canon `MultiControlledXClean` -functie die hetzelfde doel heeft voor het implementeren van een `X` door een besturings systeem beheerde bewerking, maar die gebruikmaakt van verschillende schone qubits met behulp van het `using` mechanisme.</span><span class="sxs-lookup"><span data-stu-id="41703-155">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="whats-next"></a><span data-ttu-id="41703-156">Hoe nu verder?</span><span class="sxs-lookup"><span data-stu-id="41703-156">What's Next?</span></span>
<span data-ttu-id="41703-157">Meer informatie over [controle stroom](xref:microsoft.quantum.guide.controlflow) in Q #.</span><span class="sxs-lookup"><span data-stu-id="41703-157">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>