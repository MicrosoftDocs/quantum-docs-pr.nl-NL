---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Functie _PauliBlockEncoding
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: ba30a7e87bd970961dc87f048aa586ff5c512e2a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701763"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="7d84d-102">Functie _PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="7d84d-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="7d84d-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7d84d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7d84d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d84d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d84d-105">Hiermee maakt u een Block-encoding-unitary voor een Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="7d84d-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="7d84d-106">De Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ wordt beschreven door een som van Pauli-voor waarden $P _j $, elk met een real-efficient $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="7d84d-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="7d84d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="7d84d-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="7d84d-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7d84d-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="7d84d-109">Een van `GeneratorSystem` $H $ als een som van de Pauli-voor waarden</span><span class="sxs-lookup"><span data-stu-id="7d84d-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit-adj--ctl"></a><span data-ttu-id="7d84d-110">statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="7d84d-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7d84d-111">Een unitary-bewerking $V $ waarmee de unitary $V _j $ wordt toegepast op index $ \ket{j} $, op basis van een functie $f: j\rightarrow V_j $.</span><span class="sxs-lookup"><span data-stu-id="7d84d-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit-adj--ctl---littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="7d84d-112">multiplexer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)-> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7d84d-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="7d84d-113">Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="7d84d-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="7d84d-114">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="7d84d-114">First parameter</span></span>

<span data-ttu-id="7d84d-115">De enige norm van coëfficiënten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="7d84d-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="7d84d-116">Tweede para meter</span><span class="sxs-lookup"><span data-stu-id="7d84d-116">Second parameter</span></span>

<span data-ttu-id="7d84d-117">Een `BlockEncodingReflection` unitary $U $ van de Hamiltonian $U $.</span><span class="sxs-lookup"><span data-stu-id="7d84d-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="7d84d-118">Omdat deze unitary voldoet aan $U ^ 2 = I $, is het ook een reflectie.</span><span class="sxs-lookup"><span data-stu-id="7d84d-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d84d-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7d84d-119">Remarks</span></span>

<span data-ttu-id="7d84d-120">Voor beelden van bewerkingen voor het voorbereiden en onbereid maken van de status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $, en het bouwen van een met vermenigvuldiging beheerde unitary zijn <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> en <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="7d84d-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>