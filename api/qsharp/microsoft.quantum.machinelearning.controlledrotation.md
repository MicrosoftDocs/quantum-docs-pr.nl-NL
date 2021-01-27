---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Door de gebruiker gedefinieerd ControlledRotation-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847395"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="4501e-102">Door de gebruiker gedefinieerd ControlledRotation-type</span><span class="sxs-lookup"><span data-stu-id="4501e-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="4501e-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4501e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="4501e-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4501e-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="4501e-105">Beschrijft een beheerde rotatie in termen van de doel-en besturings indexen, rotatieas en index in een model parameter vector.</span><span class="sxs-lookup"><span data-stu-id="4501e-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="4501e-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="4501e-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="4501e-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4501e-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4501e-108">Index van de doel-Qubit voor deze beheerde rotatie.</span><span class="sxs-lookup"><span data-stu-id="4501e-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="4501e-109">ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4501e-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4501e-110">Een matrix van het besturings element Qubit Indexes voor deze draaiing.</span><span class="sxs-lookup"><span data-stu-id="4501e-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="4501e-111">As: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="4501e-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="4501e-112">De as voor deze draaiing.</span><span class="sxs-lookup"><span data-stu-id="4501e-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="4501e-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4501e-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4501e-114">Een index in een model parameter vector waarmee de hoek voor deze draaiing wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="4501e-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="example"></a><span data-ttu-id="4501e-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4501e-115">Example</span></span>

<span data-ttu-id="4501e-116">Hieronder vindt u een rotatie over de $X $-as van de eerste Qubit in een REGI ster, dat wordt gecontroleerd op de tweede Qubit en met een hoek die wordt gegeven door de vierde para meter in een sequentieel model:</span><span class="sxs-lookup"><span data-stu-id="4501e-116">The following represents a rotation about the $X$-axis of the first qubit in a register, controlled on the second qubit, and with an angle given by the fourth parameter in a sequential model:</span></span>

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a><span data-ttu-id="4501e-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4501e-117">Remarks</span></span>

<span data-ttu-id="4501e-118">Een onbeheerde rotatie kan worden weer gegeven door `ControlIndices` in te stellen op een lege matrix met indexen, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="4501e-118">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>