---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Functie _DeltaParityCNOTbitstring
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701846"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="7d7b7-102">Functie _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="7d7b7-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="7d7b7-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7d7b7-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="7d7b7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d7b7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d7b7-105">Klassieke verwerkings stap van `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="7d7b7-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="7d7b7-106">Hiermee wordt een lijst met besturings element qubits voor het evalueren van het pariteits verschil tussen twee PQRS... voor waarden van even lengte.</span><span class="sxs-lookup"><span data-stu-id="7d7b7-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="7d7b7-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="7d7b7-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="7d7b7-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7d7b7-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="7d7b7-109">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7d7b7-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="7d7b7-110">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="7d7b7-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="7d7b7-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7d7b7-111">Remarks</span></span>

<span data-ttu-id="7d7b7-112">Hierbij wordt ervan uitgegaan dat de lengte van de voor waarden even is.</span><span class="sxs-lookup"><span data-stu-id="7d7b7-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="7d7b7-113">Reken lijst met besturings elementen voor het pariteits verschil tussen twee termen.</span><span class="sxs-lookup"><span data-stu-id="7d7b7-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="7d7b7-114">Hierbij wordt ervan uitgegaan dat de invoer lijsten in oplopende volg orde zijn gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="7d7b7-114">This assumes that the input lists is sorted in ascending order.</span></span>