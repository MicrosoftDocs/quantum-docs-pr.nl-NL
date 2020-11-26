---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Door de gebruiker gedefinieerd ControlledRotation-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 1e664b470caeba656ea4a73f70bbc0ef5fe76f7e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196562"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="dc3b7-102">Door de gebruiker gedefinieerd ControlledRotation-type</span><span class="sxs-lookup"><span data-stu-id="dc3b7-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="dc3b7-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc3b7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="dc3b7-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc3b7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="dc3b7-105">Beschrijft een beheerde rotatie in termen van de doel-en besturings indexen, rotatieas en index in een model parameter vector.</span><span class="sxs-lookup"><span data-stu-id="dc3b7-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="dc3b7-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="dc3b7-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="dc3b7-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc3b7-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc3b7-108">Index van de doel-Qubit voor deze beheerde rotatie.</span><span class="sxs-lookup"><span data-stu-id="dc3b7-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="dc3b7-109">ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc3b7-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc3b7-110">Een matrix van het besturings element Qubit Indexes voor deze draaiing.</span><span class="sxs-lookup"><span data-stu-id="dc3b7-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="dc3b7-111">As: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="dc3b7-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="dc3b7-112">De as voor deze draaiing.</span><span class="sxs-lookup"><span data-stu-id="dc3b7-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="dc3b7-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc3b7-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc3b7-114">Een index in een model parameter vector waarmee de hoek voor deze draaiing wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="dc3b7-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc3b7-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dc3b7-115">Remarks</span></span>

<span data-ttu-id="dc3b7-116">Een onbeheerde rotatie kan worden weer gegeven door `ControlIndices` in te stellen op een lege matrix met indexen, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="dc3b7-116">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>