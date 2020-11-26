---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: De functie PauliBlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: b1df6d239e6ef061cf0a4784c652e9dd126991d5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230426"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="317d7-102">De functie PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="317d7-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="317d7-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="317d7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="317d7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="317d7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="317d7-105">Hiermee maakt u een Block-encoding-unitary voor een Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="317d7-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="317d7-106">De Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ wordt beschreven door een som van Pauli-voor waarden $P _j $, elk met een real-efficient $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="317d7-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="317d7-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="317d7-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="317d7-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="317d7-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="317d7-109">Een van `GeneratorSystem` $H $ als een som van de Pauli-voor waarden</span><span class="sxs-lookup"><span data-stu-id="317d7-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="317d7-110">Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="317d7-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="317d7-111">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="317d7-111">First parameter</span></span>

<span data-ttu-id="317d7-112">De enige norm van coëfficiënten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="317d7-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="317d7-113">Tweede para meter</span><span class="sxs-lookup"><span data-stu-id="317d7-113">Second parameter</span></span>

<span data-ttu-id="317d7-114">Een `BlockEncodingReflection` unitary $U $ van de Hamiltonian $H $.</span><span class="sxs-lookup"><span data-stu-id="317d7-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="317d7-115">Omdat deze unitary voldoet aan $U ^ 2 = I $, is het ook een reflectie.</span><span class="sxs-lookup"><span data-stu-id="317d7-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="317d7-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="317d7-116">Remarks</span></span>

<span data-ttu-id="317d7-117">Dit wordt verkregen door de status van $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ voor te bereiden en te ontbouwen en een unitary met vermenigvuldiging <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> te maken <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="317d7-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>