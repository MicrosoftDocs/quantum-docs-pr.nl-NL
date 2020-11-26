---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: De functie TrotterStepSize
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204688"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="fcc68-102">De functie TrotterStepSize</span><span class="sxs-lookup"><span data-stu-id="fcc68-102">TrotterStepSize function</span></span>

<span data-ttu-id="fcc68-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fcc68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fcc68-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fcc68-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fcc68-105">Berekent Trotter-stap grootte in recursieve implementatie van Trotter simulatie algoritme.</span><span class="sxs-lookup"><span data-stu-id="fcc68-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="fcc68-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fcc68-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="fcc68-107">Volg orde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fcc68-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="fcc68-108">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fcc68-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="fcc68-109">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fcc68-109">Remarks</span></span>

<span data-ttu-id="fcc68-110">Deze bewerking maakt gebruik van een andere indexerings Conventie dan die van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="fcc68-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="fcc68-111">`DecomposedIntoTimeStepsCA(_, 4)`Met name overeenkomt met het scalaire $p _2 (\lambda) $ in Quant-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="fcc68-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>