---
title: Woorden lijst voor Quantum Computing
description: Een woorden lijst met algemene termen, acties en objecten die worden gebruikt in Quantum Computing.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: ba4d171d84d808f082b919dcc6156d9c65df7c05
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274502"
---
# <a name="quantum-computing-glossary"></a><span data-ttu-id="f16ea-103">Woorden lijst voor Quantum Computing</span><span class="sxs-lookup"><span data-stu-id="f16ea-103">Quantum computing glossary</span></span>

## <a name="adjoint"></a><span data-ttu-id="f16ea-104">Adjoint</span><span class="sxs-lookup"><span data-stu-id="f16ea-104">Adjoint</span></span>

<span data-ttu-id="f16ea-105">De complex geconjugeerde omzetting van een [bewerking](xref:microsoft.quantum.glossary#operation).</span><span class="sxs-lookup"><span data-stu-id="f16ea-105">The complex conjugate transpose of an [operation](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="f16ea-106">Voor bewerkingen waarbij een [unitary](xref:microsoft.quantum.glossary#unitary-operator) -operator wordt geïmplementeerd, is de adjoint de inverse van de bewerking en wordt aangegeven door een Dagger-symbool.</span><span class="sxs-lookup"><span data-stu-id="f16ea-106">For operations that implement a [unitary](xref:microsoft.quantum.glossary#unitary-operator) operator, the adjoint is the inverse of the operation and is indicated by a dagger symbol.</span></span> <span data-ttu-id="f16ea-107">Als de bewerking bijvoorbeeld `U` de operator unitary vertegenwoordigt $U $ , `Adjoint U` vertegenwoordigt $U ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="f16ea-107">For example, if the operation `U` represents the unitary operator $U$, then `Adjoint U` represents $U^\dagger$.</span></span> <span data-ttu-id="f16ea-108">Zie [adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-108">For more information, see [Adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="ancilla"></a><span data-ttu-id="f16ea-109">Ancilla</span><span class="sxs-lookup"><span data-stu-id="f16ea-109">Ancilla</span></span>

<span data-ttu-id="f16ea-110">Een [Qubit](xref:microsoft.quantum.glossary#qubit) die fungeert als tijdelijk geheugen voor een quantum computer en zo nodig wordt toegewezen en toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f16ea-110">A [qubit](xref:microsoft.quantum.glossary#qubit) that serves as temporary memory for a quantum computer and is allocated and de-allocated as needed.</span></span>  <span data-ttu-id="f16ea-111">Zie [meerdere qubits](xref:microsoft.quantum.concepts.multiple-qubits)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-111">For more information, see [Multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

## <a name="bell-state"></a><span data-ttu-id="f16ea-112">Bell-status</span><span class="sxs-lookup"><span data-stu-id="f16ea-112">Bell state</span></span>

<span data-ttu-id="f16ea-113">Een van de vier specifieke maximally [Entangled](xref:microsoft.quantum.glossary#entanglement) [Quantum-statussen](xref:microsoft.quantum.glossary#quantum-state) van twee qubits.</span><span class="sxs-lookup"><span data-stu-id="f16ea-113">One of four specific maximally [entangled](xref:microsoft.quantum.glossary#entanglement) [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two qubits.</span></span> <span data-ttu-id="f16ea-114">De vier statussen zijn gedefinieerd $ \ket { \ beta_ {IJ } } = (\Mathbb{I } \Otimes X ^ iz ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 } $.</span><span class="sxs-lookup"><span data-stu-id="f16ea-114">The four states are defined $\ket{\beta_{ij}} = (\mathbb{I} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="f16ea-115">Een Bell-status wordt ook wel een [EPR-paar](xref:microsoft.quantum.glossary#epr-pair)genoemd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-115">A Bell state is also known as an [EPR pair](xref:microsoft.quantum.glossary#epr-pair).</span></span>

## <a name="bloch-sphere"></a><span data-ttu-id="f16ea-116">Bloch-bol</span><span class="sxs-lookup"><span data-stu-id="f16ea-116">Bloch sphere</span></span>

<span data-ttu-id="f16ea-117">Een grafische weer gave van een [Quantum status](xref:microsoft.quantum.glossary#quantum-state) met één[Qubit](xref:microsoft.quantum.glossary#qubit) als een punt in een drie-dimensionale eenheid.</span><span class="sxs-lookup"><span data-stu-id="f16ea-117">A graphical representation of a single-[qubit](xref:microsoft.quantum.glossary#qubit) [quantum state](xref:microsoft.quantum.glossary#quantum-state) as a point in a three-dimensional unit sphere.</span></span> <span data-ttu-id="f16ea-118">Zie [qubits en trans formaties visualiseren met behulp van de Bloch-bol](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-118">For more information, see  [Visualizing Qubits and Transformations using the Bloch Sphere](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

## <a name="callable"></a><span data-ttu-id="f16ea-119">Aanroep bare</span><span class="sxs-lookup"><span data-stu-id="f16ea-119">Callable</span></span>

<span data-ttu-id="f16ea-120">Een [bewerking](xref:microsoft.quantum.glossary#operation) of [functie](xref:microsoft.quantum.glossary#function) in de taal Q #.</span><span class="sxs-lookup"><span data-stu-id="f16ea-120">An [operation](xref:microsoft.quantum.glossary#operation) or [function](xref:microsoft.quantum.glossary#function) in the Q# language.</span></span> <span data-ttu-id="f16ea-121">Zie [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-121">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="clifford-group"></a><span data-ttu-id="f16ea-122">Clifford-groep</span><span class="sxs-lookup"><span data-stu-id="f16ea-122">Clifford group</span></span>

<span data-ttu-id="f16ea-123">De set bewerkingen die de octants van de Bloch- [bol](xref:microsoft.quantum.glossary#bloch-sphere) in beslag nemen en permutaties van de [Pauli-Opera tors](xref:microsoft.quantum.glossary#pauli-operators).</span><span class="sxs-lookup"><span data-stu-id="f16ea-123">The set of operations that occupy the octants of the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere) and effect permutations of the [Pauli operators](xref:microsoft.quantum.glossary#pauli-operators).</span></span> <span data-ttu-id="f16ea-124">Dit zijn onder andere de bewerkingen [$X $ ](xref:microsoft.quantum.intrinsic.x), [$Y $ ](xref:microsoft.quantum.intrinsic.y), [$Z $ ](xref:microsoft.quantum.intrinsic.z), [$H $ ](xref:microsoft.quantum.intrinsic.h) en [$S $ ](xref:microsoft.quantum.intrinsic.s).</span><span class="sxs-lookup"><span data-stu-id="f16ea-124">These include the operations [$X$](xref:microsoft.quantum.intrinsic.x), [$Y$](xref:microsoft.quantum.intrinsic.y), [$Z$](xref:microsoft.quantum.intrinsic.z), [$H$](xref:microsoft.quantum.intrinsic.h) and [$S$](xref:microsoft.quantum.intrinsic.s).</span></span>

## <a name="controlled"></a><span data-ttu-id="f16ea-125">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="f16ea-125">Controlled</span></span>

<span data-ttu-id="f16ea-126">Een Quantum [bewerking](xref:microsoft.quantum.glossary#operation) waarbij een of meer [qubits](xref:microsoft.quantum.glossary#qubit) als enablers voor de doel bewerking worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f16ea-126">A quantum [operation](xref:microsoft.quantum.glossary#operation) that takes one or more [qubits](xref:microsoft.quantum.glossary#qubit) as enablers for the target operation.</span></span> <span data-ttu-id="f16ea-127">Zie [Controlled and adjoint Operations](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-127">For more information, see [Controlled and adjoint operations](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="dirac-notation"></a><span data-ttu-id="f16ea-128">Dirac-notatie</span><span class="sxs-lookup"><span data-stu-id="f16ea-128">Dirac Notation</span></span>

<span data-ttu-id="f16ea-129">Een symbolische steno waarmee de weer gave van [Quantum statussen](xref:microsoft.quantum.glossary#quantum-state), ook wel *bra-ket* notatie, wordt vereenvoudigd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-129">A symbolic shorthand that simplifies the representation of [quantum states](xref:microsoft.quantum.glossary#quantum-state), also called *bra-ket* notation.</span></span>  <span data-ttu-id="f16ea-130">Het gedeelte *Bra* vertegenwoordigt een vector van een rij, bijvoorbeeld $ \bra{A } = \begin{ bmatrix } a {_1 } & a {_2 } \end{ bmatrix } $ en het *Ket* -gedeelte vertegenwoordigt een kolom vector, $ \ket{B } = \begin{ bmatrix } b {_1 } \\ \\ B {_2 } \end{ bmatrix } $.</span><span class="sxs-lookup"><span data-stu-id="f16ea-130">The *bra* portion represents a row vector, for example  $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ and the *ket* portion represents a column vector, $\ket{B} = \begin{bmatrix} B{_1} \\\\ B{_2} \end{bmatrix}$.</span></span> <span data-ttu-id="f16ea-131">Zie [Dirac-notatie](xref:microsoft.quantum.concepts.dirac)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-131">For more information, see [Dirac Notation](xref:microsoft.quantum.concepts.dirac).</span></span>

## <a name="eigenvalue"></a><span data-ttu-id="f16ea-132">Eigenvalue</span><span class="sxs-lookup"><span data-stu-id="f16ea-132">Eigenvalue</span></span>

<span data-ttu-id="f16ea-133">De factor waarmee de grootte van een [eigenvector](xref:microsoft.quantum.glossary#eigenvector) van een bepaalde trans formatie wordt gewijzigd door de toepassing van de trans formatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-133">The factor by which the magnitude of an [eigenvector](xref:microsoft.quantum.glossary#eigenvector) of a given transformation is changed by the application of the transformation.</span></span>  <span data-ttu-id="f16ea-134">Op basis van een vier Kante matrix $M $ en een eigenvector $v $ , $MV = AVK $ , waarbij $c $ de eigenvalue is en een complex aantal argumenten kan zijn.</span><span class="sxs-lookup"><span data-stu-id="f16ea-134">Given a square matrix $M$ and an eigenvector $v$, then $Mv = cv$, where $c$ is the eigenvalue and can be a complex number of any argument.</span></span> <span data-ttu-id="f16ea-135">Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-135">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="eigenvector"></a><span data-ttu-id="f16ea-136">Eigenvector</span><span class="sxs-lookup"><span data-stu-id="f16ea-136">Eigenvector</span></span>

<span data-ttu-id="f16ea-137">Een vector waarvan de richting wordt gewijzigd door een bepaalde trans formatie en waarvan de grootte wordt gewijzigd door een factor die overeenkomt met de [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)van die vector.</span><span class="sxs-lookup"><span data-stu-id="f16ea-137">A vector whose direction is unchanged by a given transformation and whose magnitude is changed by a factor corresponding to that vector's [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue).</span></span> <span data-ttu-id="f16ea-138">Op basis van een vier Kante matrix $M $ en een eigenvalue $c $ , $MV = AVK $ , waarbij $v $ een eigenvector van de matrix is en een complex aantal argumenten kan zijn.</span><span class="sxs-lookup"><span data-stu-id="f16ea-138">Given a square matrix $M$ and an eigenvalue $c$, then $Mv = cv$, where $v$ is an eigenvector of the matrix and can be a complex number of any argument.</span></span> <span data-ttu-id="f16ea-139">Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-139">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="entanglement"></a><span data-ttu-id="f16ea-140">Verstrengeling</span><span class="sxs-lookup"><span data-stu-id="f16ea-140">Entanglement</span></span>

<span data-ttu-id="f16ea-141">Quantum deeltjes, zoals [qubits](xref:microsoft.quantum.glossary#qubit), kunnen worden aangesloten of *Entangled* , zodat ze onafhankelijk van elkaar kunnen worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="f16ea-141">Quantum particles, such as [qubits](xref:microsoft.quantum.glossary#qubit), can be connected or *entangled* such that they cannot be described independently from each other.</span></span> <span data-ttu-id="f16ea-142">De meet resultaten worden ook gecorreleerd wanneer ze oneindig ver van elkaar zijn gescheiden.</span><span class="sxs-lookup"><span data-stu-id="f16ea-142">Their measurement results are correlated even when they are separated infinitely far away.</span></span> <span data-ttu-id="f16ea-143">Entanglement is essentieel om de [status](xref:microsoft.quantum.glossary#quantum-state) van een Qubit te [meten](xref:microsoft.quantum.glossary#measurement) .</span><span class="sxs-lookup"><span data-stu-id="f16ea-143">Entanglement is essential to [measuring](xref:microsoft.quantum.glossary#measurement) the [state](xref:microsoft.quantum.glossary#quantum-state) of a qubit.</span></span>  <span data-ttu-id="f16ea-144">Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-144">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="epr-pair"></a><span data-ttu-id="f16ea-145">EPR paar</span><span class="sxs-lookup"><span data-stu-id="f16ea-145">EPR pair</span></span>

<span data-ttu-id="f16ea-146">Een van de vier specifieke maximally Entangled [Quantum-statussen](xref:microsoft.quantum.glossary#quantum-state) van twee [qubits](xref:microsoft.quantum.glossary#qubit).</span><span class="sxs-lookup"><span data-stu-id="f16ea-146">One of four specific maximally entangled [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two [qubits](xref:microsoft.quantum.glossary#qubit).</span></span> <span data-ttu-id="f16ea-147">De vier statussen zijn gedefinieerd $ \ket { \ beta_ {IJ } } = (\Mathbb{1 } \Otimes X ^ iz ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 } $.</span><span class="sxs-lookup"><span data-stu-id="f16ea-147">The four states are defined $\ket{\beta_{ij}} = (\mathbb{1} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="f16ea-148">Een EPR-paar wordt ook wel een [Bell-status](xref:microsoft.quantum.glossary#bell-state) genoemd</span><span class="sxs-lookup"><span data-stu-id="f16ea-148">An EPR pair is also known as a [Bell state](xref:microsoft.quantum.glossary#bell-state)</span></span>

## <a name="evolution"></a><span data-ttu-id="f16ea-149">Evolutie</span><span class="sxs-lookup"><span data-stu-id="f16ea-149">Evolution</span></span>

<span data-ttu-id="f16ea-150">Hoe een [Quantum status](xref:microsoft.quantum.glossary#quantum-state) in de loop van de tijd verandert.</span><span class="sxs-lookup"><span data-stu-id="f16ea-150">How a [quantum state](xref:microsoft.quantum.glossary#quantum-state) changes over time.</span></span> <span data-ttu-id="f16ea-151">Zie [matrix exponentiëlen](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-151">For more information, see [Matrix exponentials](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).</span></span>

## <a name="function"></a><span data-ttu-id="f16ea-152">Functie</span><span class="sxs-lookup"><span data-stu-id="f16ea-152">Function</span></span>
<span data-ttu-id="f16ea-153">Een type subroutine in de Q #-taal die louter klassiek (niet-Quantum) is.</span><span class="sxs-lookup"><span data-stu-id="f16ea-153">A type of subroutine in the Q# language that is purely classical (non-quantum).</span></span> <span data-ttu-id="f16ea-154">Terwijl functies worden gebruikt binnen Quantum algoritmen, kunnen ze niet reageren op [qubits](xref:microsoft.quantum.glossary#qubit) of aanroep [bewerkingen](xref:microsoft.quantum.glossary#operation).</span><span class="sxs-lookup"><span data-stu-id="f16ea-154">While functions are used within quantum algorithms, they cannot act on [qubits](xref:microsoft.quantum.glossary#qubit) or call [operations](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="f16ea-155">Zie [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-155">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="gate"></a><span data-ttu-id="f16ea-156">Poort</span><span class="sxs-lookup"><span data-stu-id="f16ea-156">Gate</span></span>

<span data-ttu-id="f16ea-157">Een verouderde term voor een Quantum [bewerking](xref:microsoft.quantum.glossary#operation), gebaseerd op het concept van klassieke logische poorten.</span><span class="sxs-lookup"><span data-stu-id="f16ea-157">A legacy term for a quantum [operation](xref:microsoft.quantum.glossary#operation), based on the concept of classical logic gates.</span></span> <span data-ttu-id="f16ea-158">Een [Quantum circuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is een netwerk van Gates (of bewerkingen), op basis van het vergelijk bare concept van klassieke logica-circuits.</span><span class="sxs-lookup"><span data-stu-id="f16ea-158">A [quantum circuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is a network of gates (or operations), based on the similar concept of classical logic circuits.</span></span>

## <a name="global-phase"></a><span data-ttu-id="f16ea-159">Globale fase</span><span class="sxs-lookup"><span data-stu-id="f16ea-159">Global phase</span></span>

<span data-ttu-id="f16ea-160">Wanneer twee [statussen](xref:microsoft.quantum.glossary#quantum-state) gelijk zijn aan een veelvoud van een complex getal $e ^ {i \phi } $, worden ze in een wereld wijde fase onderscheiden.</span><span class="sxs-lookup"><span data-stu-id="f16ea-160">When two [states](xref:microsoft.quantum.glossary#quantum-state) are identical up to a multiple of a complex number $e^{i\phi}$, they are said to differ up to a global phase.</span></span> <span data-ttu-id="f16ea-161">In tegens telling tot lokale fasen kunnen globale fasen niet worden geobserveerd met behulp van enige [meet](xref:microsoft.quantum.glossary#measurement)periode.</span><span class="sxs-lookup"><span data-stu-id="f16ea-161">Unlike local phases, global phases cannot be observed through any [measurment](xref:microsoft.quantum.glossary#measurement).</span></span> <span data-ttu-id="f16ea-162">Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-162">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="hadamard"></a><span data-ttu-id="f16ea-163">Hadamard</span><span class="sxs-lookup"><span data-stu-id="f16ea-163">Hadamard</span></span>

<span data-ttu-id="f16ea-164">De Hadamard-bewerking (ook wel de Hadamard-Gate of trans formatie genoemd) werkt op één [Qubit](xref:microsoft.quantum.glossary#qubit) en plaatst deze in een even super [positie](xref:microsoft.quantum.glossary#superposition) van $ \ket{0 } $ of $ \ket{1 } $ als de Qubit in eerste instantie de status $ \ket{0 $ heeft } .</span><span class="sxs-lookup"><span data-stu-id="f16ea-164">The Hadamard operation (also referred to as the Hadamard gate or transform) acts on a single [qubit](xref:microsoft.quantum.glossary#qubit) and puts it in an even [superposition](xref:microsoft.quantum.glossary#superposition) of $\ket{0}$ or $\ket{1}$ if the qubit is initially in the $\ket{0}$ state.</span></span> <span data-ttu-id="f16ea-165">In Q # wordt deze bewerking toegepast door de vooraf gedefinieerde [`H`](xref:microsoft.quantum.intrinsic.h) bewerking.</span><span class="sxs-lookup"><span data-stu-id="f16ea-165">In Q#, this operation is applied by the pre-defined [`H`](xref:microsoft.quantum.intrinsic.h) operation.</span></span>

## <a name="immutable"></a><span data-ttu-id="f16ea-166">Onveranderbare</span><span class="sxs-lookup"><span data-stu-id="f16ea-166">Immutable</span></span>

<span data-ttu-id="f16ea-167">Een variabele waarvan de waarde niet kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-167">A variable whose value cannot be changed.</span></span> <span data-ttu-id="f16ea-168">Een onveranderbare variabele in Q # wordt gemaakt met behulp van het `let` sleutel woord.</span><span class="sxs-lookup"><span data-stu-id="f16ea-168">An immutable variable in Q# is created using the `let` keyword.</span></span> <span data-ttu-id="f16ea-169">Als u variabelen wilt declareren die *kunnen* worden gewijzigd, gebruikt u het sleutel woord [onveranderbaar](xref:microsoft.quantum.glossary#immutable) om te declareren en het `set` tref woord om de waarde te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f16ea-169">To declare variables that *can* be changed, use the [mutable](xref:microsoft.quantum.glossary#immutable) keyword to declare and the `set` keyword to modify the value.</span></span> 

## <a name="measurement"></a><span data-ttu-id="f16ea-170">Meting</span><span class="sxs-lookup"><span data-stu-id="f16ea-170">Measurement</span></span>

<span data-ttu-id="f16ea-171">Een manipulatie van een [Qubit](xref:microsoft.quantum.glossary#qubit) (of set qubits) die het resultaat van een waarneming oplevert, in feite het verkrijgen van een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="f16ea-171">A manipulation of a [qubit](xref:microsoft.quantum.glossary#qubit) (or set of qubits) that yields the result of an observation, in effect obtaining a classical bit.</span></span> <span data-ttu-id="f16ea-172">Zie [de Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-172">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).</span></span>

## <a name="mutable"></a><span data-ttu-id="f16ea-173">Veranderlijk</span><span class="sxs-lookup"><span data-stu-id="f16ea-173">Mutable</span></span>

<span data-ttu-id="f16ea-174">Een variabele waarvan de waarde kan worden gewijzigd nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f16ea-174">A variable whose value may be changed after it is created.</span></span> <span data-ttu-id="f16ea-175">Een onveranderlijke variabele in Q # wordt gedeclareerd met het `mutable` sleutel woord en gewijzigd met het `set` sleutel woord.</span><span class="sxs-lookup"><span data-stu-id="f16ea-175">A mutable variable in Q# is declared using the `mutable` keyword and modified using the `set` keyword.</span></span> <span data-ttu-id="f16ea-176">Variabelen die met het `let` sleutel woord zijn gemaakt, zijn [onveranderbaar](xref:microsoft.quantum.glossary#immutable) en hun waarde kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-176">Variables created with the `let` keyword are [immutable](xref:microsoft.quantum.glossary#immutable) and their value cannot be changed.</span></span>

## <a name="namespace"></a><span data-ttu-id="f16ea-177">Naamruimte</span><span class="sxs-lookup"><span data-stu-id="f16ea-177">Namespace</span></span>

<span data-ttu-id="f16ea-178">Een label voor een verzameling verwante namen (bijvoorbeeld [bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function)en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type)).</span><span class="sxs-lookup"><span data-stu-id="f16ea-178">A label for a collection of related names (i.e., [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function), and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type)).</span></span> <span data-ttu-id="f16ea-179">Voor de naam ruimte [micro soft. Quantum. prepare](xref:microsoft.quantum.preparation) etiketten worden alle symbolen in de standaard bibliotheek beschreven die u helpen bij het voorbereiden van initiële statussen.</span><span class="sxs-lookup"><span data-stu-id="f16ea-179">For instance the namespace [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) labels all of the symbols defined in the standard library that help with preparing initial states.</span></span>

## <a name="operation"></a><span data-ttu-id="f16ea-180">Bewerking</span><span class="sxs-lookup"><span data-stu-id="f16ea-180">Operation</span></span>

<span data-ttu-id="f16ea-181">De basis eenheid voor het uitvoeren van quantums in Q #.</span><span class="sxs-lookup"><span data-stu-id="f16ea-181">The basic unit of quantum execution in Q#.</span></span> <span data-ttu-id="f16ea-182">Het is ongeveer gelijk aan een functie in C, C++ of python, of een statische methode in C# of Java.</span><span class="sxs-lookup"><span data-stu-id="f16ea-182">It is roughly equivalent to a function in C, C++ or Python, or a static method in C# or Java.</span></span> <span data-ttu-id="f16ea-183">Zie [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-183">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="operator-application"></a><span data-ttu-id="f16ea-184">Operator toepassing</span><span class="sxs-lookup"><span data-stu-id="f16ea-184">Operator application</span></span>

<span data-ttu-id="f16ea-185">Een Quantum bewerking wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-185">Performing a quantum operation.</span></span> <span data-ttu-id="f16ea-186">Dit past doorgaans een unitary-matrix toe op de huidige Quantum-status vector.</span><span class="sxs-lookup"><span data-stu-id="f16ea-186">This typically applies a unitary matrix to the current quantum state vector.</span></span>

## <a name="oracle"></a><span data-ttu-id="f16ea-187">Oracle</span><span class="sxs-lookup"><span data-stu-id="f16ea-187">Oracle</span></span>

<span data-ttu-id="f16ea-188">Een subroutine die gegevens afhankelijke informatie levert aan een Quantum algoritme tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="f16ea-188">A subroutine that provides data-dependent information to a quantum algorithm at runtime.</span></span> <span data-ttu-id="f16ea-189">Normaal gesp roken is het doel om een [superpositie](xref:microsoft.quantum.glossary#superposition) van uitvoer te bieden die overeenkomt met de invoer die zich in superpositie bevindt.</span><span class="sxs-lookup"><span data-stu-id="f16ea-189">Typically, the goal is to provide a [superposition](xref:microsoft.quantum.glossary#superposition) of outputs corresponding to inputs that are in superposition.</span></span> <span data-ttu-id="f16ea-190">Zie voor meer informatie [Oracle](xref:microsoft.quantum.libraries.data-structures#oracles).</span><span class="sxs-lookup"><span data-stu-id="f16ea-190">For more information, see [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).</span></span>

## <a name="partial-application"></a><span data-ttu-id="f16ea-191">Gedeeltelijke toepassing</span><span class="sxs-lookup"><span data-stu-id="f16ea-191">Partial application</span></span>

<span data-ttu-id="f16ea-192">Het aanroepen van een [functie](xref:microsoft.quantum.glossary#function) of [bewerking](xref:microsoft.quantum.glossary#operation) zonder de vereiste invoer.</span><span class="sxs-lookup"><span data-stu-id="f16ea-192">Calling a [function](xref:microsoft.quantum.glossary#function) or [operation](xref:microsoft.quantum.glossary#operation) without all the required inputs.</span></span> <span data-ttu-id="f16ea-193">Hiermee wordt een nieuwe [aanroep](xref:microsoft.quantum.glossary#callable) geretourneerd waarvoor alleen de ontbrekende para meters (aangegeven door een onderstrepings teken) moeten worden opgegeven tijdens een toekomstige toepassing.</span><span class="sxs-lookup"><span data-stu-id="f16ea-193">This returns a new [callable](xref:microsoft.quantum.glossary#callable) that only needs the missing parameters (indicated by an underscore) to be supplied during a future application.</span></span> <span data-ttu-id="f16ea-194">Als u bijvoorbeeld de functie hebt opgegeven, `MyFunc(x : int, y : int) : int {return x + y;}` kunt u deze gedeeltelijk Toep assen op een nieuwe functie `let NewFunc = MyFunc(_, 3)` .</span><span class="sxs-lookup"><span data-stu-id="f16ea-194">For example, given the function `MyFunc(x : int, y : int) : int {return x + y;}` you can partially apply it to a new function `let NewFunc = MyFunc(_, 3)`.</span></span> <span data-ttu-id="f16ea-195">U kunt de nieuwe functie vervolgens op een later tijdstip aanroepen met de ontbrekende para meter, `NewFunc(2)` waarmee de waarde *5*wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-195">You can then call the new function at a later time with the missing parameter `NewFunc(2)` which returns the value *5*.</span></span>  <span data-ttu-id="f16ea-196">Zie voor meer informatie [gedeeltelijke toepassing](xref:microsoft.quantum.guide.operationsfunctions#partial-application).</span><span class="sxs-lookup"><span data-stu-id="f16ea-196">For more information, see [Partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application).</span></span>

## <a name="pauli-operators"></a><span data-ttu-id="f16ea-197">Pauli-Opera tors</span><span class="sxs-lookup"><span data-stu-id="f16ea-197">Pauli operators</span></span>

<span data-ttu-id="f16ea-198">Een set van drie unitary matrices met een matrix die de en de `X` Quantum-bewerkingen wordt genoemd `Y` `Z` .</span><span class="sxs-lookup"><span data-stu-id="f16ea-198">A set of three 2 x 2 unitary matrices known as the `X`, `Y` and `Z` quantum operations.</span></span> <span data-ttu-id="f16ea-199">De ID-matrix, $I $ , wordt vaak ook opgenomen in de set.</span><span class="sxs-lookup"><span data-stu-id="f16ea-199">The identity matrix, $I$, is often included in the set as well.</span></span>  <span data-ttu-id="f16ea-200">$I = \begin{ bmatrix } 1 & 0 \\ \\ 0 & 1 \end{ bmatrix } $, $X = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } $, $Y = \begin{ bmatrix } 0 &-i \\ \\ i & 0 \end{ bmatrix } $, $Z = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } $.</span><span class="sxs-lookup"><span data-stu-id="f16ea-200">$I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix}$, $X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}$, $Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix}$, $Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}$.</span></span>   <span data-ttu-id="f16ea-201">Zie [Single-Qubit Operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-201">For more information, see [Single-qubit operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span></span>

## <a name="quantum-circuit-diagram"></a><span data-ttu-id="f16ea-202">Quantum circuit diagram</span><span class="sxs-lookup"><span data-stu-id="f16ea-202">Quantum circuit diagram</span></span>

<span data-ttu-id="f16ea-203">Een methode voor het grafisch weer geven van de volg orde van de [bewerkingen](xref:microsoft.quantum.glossary#operation) (of [poorten](xref:microsoft.quantum.glossary#gate)) voor eenvoudige Quantum-Program ma's, bijvoorbeeld</span><span class="sxs-lookup"><span data-stu-id="f16ea-203">A method to graphically represent the sequence of [operations](xref:microsoft.quantum.glossary#operation) (or [gates](xref:microsoft.quantum.glossary#gate)) for simple quantum programs, for example</span></span> 

![Voorbeeld diagram van circuit](~/media/qpe.png)<span data-ttu-id="f16ea-205">.</span><span class="sxs-lookup"><span data-stu-id="f16ea-205">.</span></span> 

<span data-ttu-id="f16ea-206">Zie [Quantum circuits](xref:microsoft.quantum.concepts.circuits)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-206">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits).</span></span>

## <a name="quantum-libraries"></a><span data-ttu-id="f16ea-207">Quantum bibliotheken</span><span class="sxs-lookup"><span data-stu-id="f16ea-207">Quantum libraries</span></span>

<span data-ttu-id="f16ea-208">Verzamelingen [bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function) en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type) voor het maken van Q #-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="f16ea-208">Collections of [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) for creating Q# programs.</span></span> <span data-ttu-id="f16ea-209">De [standaard bibliotheek](xref:microsoft.quantum.libraries.standard.intro) wordt standaard geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-209">The [Standard library](xref:microsoft.quantum.libraries.standard.intro) is installed by default.</span></span> <span data-ttu-id="f16ea-210">Andere beschik bare bibliotheken zijn de [bibliotheek voor schei kunde](xref:microsoft.quantum.chemistry.concepts.intro), de [numerieke bibliotheek](xref:microsoft.quantum.numerics.intro) en de [machine learning-bibliotheek](xref:microsoft.quantum.machine-learning.concepts.intro).</span><span class="sxs-lookup"><span data-stu-id="f16ea-210">Other libraries available are the [Chemistry library](xref:microsoft.quantum.chemistry.concepts.intro), the [Numerics library](xref:microsoft.quantum.numerics.intro) and the [Machine learning library](xref:microsoft.quantum.machine-learning.concepts.intro).</span></span>

## <a name="quantum-state"></a><span data-ttu-id="f16ea-211">Quantum status</span><span class="sxs-lookup"><span data-stu-id="f16ea-211">Quantum state</span></span>

<span data-ttu-id="f16ea-212">De nauw keurige status van een geïsoleerd Quantum systeem, waaruit [meting](xref:microsoft.quantum.glossary#measurement) kansen kunnen worden geëxtraheerd.</span><span class="sxs-lookup"><span data-stu-id="f16ea-212">The precise state of an isolated quantum system, from which [measurement](xref:microsoft.quantum.glossary#measurement) probabilities can be extracted.</span></span> <span data-ttu-id="f16ea-213">In Quantum Computing gebruikt de Quantum Simulator deze informatie om te simuleren hoe qubits reageert op bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="f16ea-213">In quantum computing, the quantum simulator uses this information to simulate how qubits respond to operations.</span></span> <span data-ttu-id="f16ea-214">Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-214">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="qubit"></a><span data-ttu-id="f16ea-215">Qubit</span><span class="sxs-lookup"><span data-stu-id="f16ea-215">Qubit</span></span>

<span data-ttu-id="f16ea-216">Een eenvoudige eenheid van quantum informatie, vergelijkbaar met een *bit* in klassieke computing.</span><span class="sxs-lookup"><span data-stu-id="f16ea-216">A basic unit of quantum information, analogous to a *bit* in classical computing.</span></span> <span data-ttu-id="f16ea-217">Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-217">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="repeat-until-success"></a><span data-ttu-id="f16ea-218">Herhalen-tot-geslaagd</span><span class="sxs-lookup"><span data-stu-id="f16ea-218">Repeat-until-success</span></span>

<span data-ttu-id="f16ea-219">Een Quantum algoritme dat probabilistically slaagt.</span><span class="sxs-lookup"><span data-stu-id="f16ea-219">A quantum algorithm that probabilistically succeeds.</span></span> <span data-ttu-id="f16ea-220">Als de routine is mislukt, wordt het opnieuw geprobeerd tot geslaagd (of is er een limiet bereikt).</span><span class="sxs-lookup"><span data-stu-id="f16ea-220">Upon failure, the routine will retry until successful (or a limit has been reached).</span></span> <span data-ttu-id="f16ea-221">Zie [herhalen tot geslaagd (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="f16ea-221">For more information, see [Repeat Until Success (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)</span></span>

## <a name="standard-libraries"></a><span data-ttu-id="f16ea-222">Standaardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="f16ea-222">Standard libraries</span></span>

<span data-ttu-id="f16ea-223">[Bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function) en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type) die samen met de Q #-compiler worden geïnstalleerd tijdens de installatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-223">[Operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) that are installed along with the Q# compiler during installation.</span></span> <span data-ttu-id="f16ea-224">De implementatie van de standaard bibliotheek is neutraal met betrekking tot doel computers.</span><span class="sxs-lookup"><span data-stu-id="f16ea-224">The standard library implementation is agnostic with respect to target machines.</span></span> <span data-ttu-id="f16ea-225">Zie [standaard bibliotheken](xref:microsoft.quantum.libraries.standard.intro)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-225">For more information, see [Standard libraries](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="superposition"></a><span data-ttu-id="f16ea-226">Superpositie</span><span class="sxs-lookup"><span data-stu-id="f16ea-226">Superposition</span></span>

<span data-ttu-id="f16ea-227">Het concept in het quantum computing dat een [Qubit](xref:microsoft.quantum.glossary#qubit) is een lineaire combi natie van twee staten, $ \ket{0 } $ en $ \ket{1 } $, totdat deze wordt [gemeten](xref:microsoft.quantum.glossary#measurement).</span><span class="sxs-lookup"><span data-stu-id="f16ea-227">The concept in quantum computing that a [qubit](xref:microsoft.quantum.glossary#qubit) is a linear combination of two states, $\ket{0}$ and $\ket{1}$, until it is [measured](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="f16ea-228">Zie [informatie over Quantum Computing](xref:microsoft.quantum.overview.understanding)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-228">For more information, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding).</span></span>

## <a name="target-machine"></a><span data-ttu-id="f16ea-229">Doel computer</span><span class="sxs-lookup"><span data-stu-id="f16ea-229">Target machine</span></span>

<span data-ttu-id="f16ea-230">Een compilatie doel dat een abstract Quantum programma verlaagt naar hardware of simulatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-230">A compilation target that lowers an abstract quantum program towards hardware or simulation.</span></span> <span data-ttu-id="f16ea-231">Dit omvat doorgaans herschrijf bewerkingen voor veel doelen, waaronder het vervangen van een Gate, code ring voor fout correctie, geometrische indeling en andere.</span><span class="sxs-lookup"><span data-stu-id="f16ea-231">This typically include re-writes for many purposes including gate replacement, encoding for error correction, geometric layout and others.</span></span> <span data-ttu-id="f16ea-232">Zie [Quantum simulators and host Applications](xref:microsoft.quantum.machines)(Engelstalig) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-232">For more information, see [Quantum simulators and host applications](xref:microsoft.quantum.machines).</span></span>

## <a name="teleportation"></a><span data-ttu-id="f16ea-233">Teleportatie</span><span class="sxs-lookup"><span data-stu-id="f16ea-233">Teleportation</span></span>

<span data-ttu-id="f16ea-234">Een methode voor het opnieuw genereren van gegevens, of de [Quantum status](xref:microsoft.quantum.glossary#quantum-state), van een [Qubit](xref:microsoft.quantum.glossary#qubit) van de ene locatie naar een andere zonder fysiek de Qubit te verplaatsen, met [entanglement](xref:microsoft.quantum.glossary#entanglement) en [meting](xref:microsoft.quantum.glossary#measurement).</span><span class="sxs-lookup"><span data-stu-id="f16ea-234">A method for regenerating data, or the [quantum state](xref:microsoft.quantum.glossary#quantum-state), of one [qubit](xref:microsoft.quantum.glossary#qubit) from one place to another without physically moving the qubit, using [entanglement](xref:microsoft.quantum.glossary#entanglement) and [measurement](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="f16ea-235">Zie [Quantum circuits](xref:microsoft.quantum.concepts.circuits) en de respectieve Kata bij [Quantum Katas](xref:microsoft.quantum.overview.katas)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-235">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits) and the respective kata at [Quantum Katas](xref:microsoft.quantum.overview.katas).</span></span>

## <a name="tuple"></a><span data-ttu-id="f16ea-236">Kaart</span><span class="sxs-lookup"><span data-stu-id="f16ea-236">Tuple</span></span>

<span data-ttu-id="f16ea-237">Een verzameling door komma's gescheiden waarden die fungeert als een enkele waarde.</span><span class="sxs-lookup"><span data-stu-id="f16ea-237">A collection of comma-separated values that acts as a single value.</span></span> <span data-ttu-id="f16ea-238">Het *type* van een tuple wordt gedefinieerd door de typen waarden die deze bevat.</span><span class="sxs-lookup"><span data-stu-id="f16ea-238">The *type* of a tuple is defined by the types of values it contains.</span></span> <span data-ttu-id="f16ea-239">In Q # zijn Tuples [onveranderbaar](xref:microsoft.quantum.glossary#immutable) en kunnen ze zijn genest, matrices bevatten of in een matrix worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f16ea-239">In Q#, tuples are [immutable](xref:microsoft.quantum.glossary#immutable) and can be nested, contain arrays, or used in an array.</span></span> <span data-ttu-id="f16ea-240">Zie voor meer informatie [tuple types](xref:microsoft.quantum.guide.types#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="f16ea-240">For more information, see [Tuple types](xref:microsoft.quantum.guide.types#tuple-types).</span></span>

## <a name="unitary-operator"></a><span data-ttu-id="f16ea-241">Unitary-operator</span><span class="sxs-lookup"><span data-stu-id="f16ea-241">Unitary operator</span></span>

<span data-ttu-id="f16ea-242">Een operator waarvan de inverse is gelijk aan de [adjoint](xref:microsoft.quantum.glossary#adjoint), d.w.z. $uu ^ {\dagger } = \id $ .</span><span class="sxs-lookup"><span data-stu-id="f16ea-242">An operator whose inverse is equal to its [adjoint](xref:microsoft.quantum.glossary#adjoint), i.e., $UU^{\dagger} = \id$.</span></span>

## <a name="user-defined-type"></a><span data-ttu-id="f16ea-243">Door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="f16ea-243">User-defined type</span></span>

<span data-ttu-id="f16ea-244">Een verzameling van ingebouwde of eerder gedefinieerde typen die als één eenheid kunnen worden aangeduid.</span><span class="sxs-lookup"><span data-stu-id="f16ea-244">A collection of built-in or previously defined types that may be referred to as a single unit.</span></span> <span data-ttu-id="f16ea-245">Zie door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.guide.types#user-defined-types)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16ea-245">For more information, see [User-defined types](xref:microsoft.quantum.guide.types#user-defined-types).</span></span>