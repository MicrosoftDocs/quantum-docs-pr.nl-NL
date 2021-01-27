---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: De functie PauliBlockEncoding
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848009"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="edda3-102">De functie PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="edda3-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="edda3-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="edda3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="edda3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="edda3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="edda3-105">Hiermee maakt u een Block-encoding-unitary voor een Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="edda3-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="edda3-106">De Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ wordt beschreven door een som van Pauli-voor waarden $P _j $, elk met een real-efficient $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="edda3-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="edda3-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="edda3-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="edda3-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="edda3-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="edda3-109">Een van `GeneratorSystem` $H $ als een som van de Pauli-voor waarden</span><span class="sxs-lookup"><span data-stu-id="edda3-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="edda3-110">Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="edda3-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="edda3-111">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="edda3-111">First parameter</span></span>

<span data-ttu-id="edda3-112">De enige norm van coëfficiënten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="edda3-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="edda3-113">Tweede para meter</span><span class="sxs-lookup"><span data-stu-id="edda3-113">Second parameter</span></span>

<span data-ttu-id="edda3-114">Een `BlockEncodingReflection` unitary $U $ van de Hamiltonian $H $.</span><span class="sxs-lookup"><span data-stu-id="edda3-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="edda3-115">Omdat deze unitary voldoet aan $U ^ 2 = I $, is het ook een reflectie.</span><span class="sxs-lookup"><span data-stu-id="edda3-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="edda3-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="edda3-116">Remarks</span></span>

<span data-ttu-id="edda3-117">Dit wordt verkregen door de status van $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ voor te bereiden en te ontbouwen en een unitary met vermenigvuldiging <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> te maken <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="edda3-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>