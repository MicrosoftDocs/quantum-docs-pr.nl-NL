---
uid: Microsoft.Quantum.Math.PNormalized
title: De functie PNormalized
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 6f9dfebe83f52cbf486cd8e6874d3699f5e6b8ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707915"
---
# <a name="pnormalized-function"></a><span data-ttu-id="10d7c-102">De functie PNormalized</span><span class="sxs-lookup"><span data-stu-id="10d7c-102">PNormalized function</span></span>

<span data-ttu-id="10d7c-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="10d7c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="10d7c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10d7c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10d7c-105">Normaliseert een vector van `Double` s in de `L(p)` norm.</span><span class="sxs-lookup"><span data-stu-id="10d7c-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="10d7c-106">Op basis van een matrix $x $ van type, wordt hiermee `Double[]` een matrix geretourneerd waarin alle elementen worden gedeeld door de $p $-norm $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="10d7c-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="10d7c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="10d7c-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="10d7c-108">p: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="10d7c-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="10d7c-109">De exponent $p $ in de $p $-norm.</span><span class="sxs-lookup"><span data-stu-id="10d7c-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="10d7c-110">matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="10d7c-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="10d7c-111">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="10d7c-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="10d7c-112">De matrix $x $ genormaliseerd door de $p $-norm $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="10d7c-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="10d7c-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="10d7c-113">See Also</span></span>

- [<span data-ttu-id="10d7c-114">Micro soft. Quantum. math. PNorm</span><span class="sxs-lookup"><span data-stu-id="10d7c-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)