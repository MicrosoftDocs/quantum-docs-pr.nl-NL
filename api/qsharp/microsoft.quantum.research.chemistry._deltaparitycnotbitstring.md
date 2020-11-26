---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Functie _DeltaParityCNOTbitstring
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226074"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="5e67b-102">Functie _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="5e67b-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="5e67b-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5e67b-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="5e67b-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5e67b-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="5e67b-105">Klassieke verwerkings stap van `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="5e67b-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="5e67b-106">Hiermee wordt een lijst met besturings element qubits voor het evalueren van het pariteits verschil tussen twee PQRS... voor waarden van even lengte.</span><span class="sxs-lookup"><span data-stu-id="5e67b-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="5e67b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5e67b-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="5e67b-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5e67b-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="5e67b-109">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5e67b-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="5e67b-110">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="5e67b-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="5e67b-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5e67b-111">Remarks</span></span>

<span data-ttu-id="5e67b-112">Hierbij wordt ervan uitgegaan dat de lengte van de voor waarden even is.</span><span class="sxs-lookup"><span data-stu-id="5e67b-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="5e67b-113">Reken lijst met besturings elementen voor het pariteits verschil tussen twee termen.</span><span class="sxs-lookup"><span data-stu-id="5e67b-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="5e67b-114">Hierbij wordt ervan uitgegaan dat de invoer lijsten in oplopende volg orde zijn gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="5e67b-114">This assumes that the input lists is sorted in ascending order.</span></span>