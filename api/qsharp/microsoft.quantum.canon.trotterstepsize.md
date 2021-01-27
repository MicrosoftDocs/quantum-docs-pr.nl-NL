---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: De functie TrotterStepSize
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840079"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="e8520-102">De functie TrotterStepSize</span><span class="sxs-lookup"><span data-stu-id="e8520-102">TrotterStepSize function</span></span>

<span data-ttu-id="e8520-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8520-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8520-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8520-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8520-105">Berekent Trotter-stap grootte in recursieve implementatie van Trotter simulatie algoritme.</span><span class="sxs-lookup"><span data-stu-id="e8520-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="e8520-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e8520-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="e8520-107">Volg orde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e8520-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="e8520-108">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e8520-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="e8520-109">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e8520-109">Remarks</span></span>

<span data-ttu-id="e8520-110">Deze bewerking maakt gebruik van een andere indexerings Conventie dan die van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="e8520-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="e8520-111">`DecomposedIntoTimeStepsCA(_, 4)`Met name overeenkomt met het scalaire $p _2 (\lambda) $ in Quant-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="e8520-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>