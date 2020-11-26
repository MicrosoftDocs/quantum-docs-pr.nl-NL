---
uid: Microsoft.Quantum.Math.SquaredNorm
title: De functie SquaredNorm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: ecbc66a8851f23187e0c0ea53ce121442323733b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227298"
---
# <a name="squarednorm-function"></a><span data-ttu-id="bc8a4-102">De functie SquaredNorm</span><span class="sxs-lookup"><span data-stu-id="bc8a4-102">SquaredNorm function</span></span>

<span data-ttu-id="bc8a4-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bc8a4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bc8a4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc8a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc8a4-105">Retourneert de vier Kante 2-norm van een vector.</span><span class="sxs-lookup"><span data-stu-id="bc8a4-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="bc8a4-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bc8a4-106">Description</span></span>

<span data-ttu-id="bc8a4-107">Retourneert de vier Kante 2-norm van een vector; op basis van de invoer $ \vec{x} $ retourneert $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="bc8a4-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="bc8a4-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="bc8a4-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="bc8a4-109">matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bc8a4-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bc8a4-110">De vector waarvan het kwadraat 2-norm moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="bc8a4-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="bc8a4-111">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bc8a4-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bc8a4-112">De vier Kante 2-norm van `array` .</span><span class="sxs-lookup"><span data-stu-id="bc8a4-112">The squared 2-norm of `array`.</span></span>