---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Functie _DeltaParityCNOTbitstring
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847606"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="5bbd4-102">Functie _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="5bbd4-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="5bbd4-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="5bbd4-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="5bbd4-105">Klassieke verwerkings stap van `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="5bbd4-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="5bbd4-106">Hiermee wordt een lijst met besturings element qubits voor het evalueren van het pariteits verschil tussen twee PQRS... voor waarden van even lengte.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="5bbd4-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5bbd4-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="5bbd4-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bbd4-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="5bbd4-109">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bbd4-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="5bbd4-110">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="5bbd4-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="5bbd4-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5bbd4-111">Remarks</span></span>

<span data-ttu-id="5bbd4-112">Hierbij wordt ervan uitgegaan dat de lengte van de voor waarden even is.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="5bbd4-113">Reken lijst met besturings elementen voor het pariteits verschil tussen twee termen.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="5bbd4-114">Hierbij wordt ervan uitgegaan dat de invoer lijsten in oplopende volg orde zijn gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-114">This assumes that the input lists is sorted in ascending order.</span></span>