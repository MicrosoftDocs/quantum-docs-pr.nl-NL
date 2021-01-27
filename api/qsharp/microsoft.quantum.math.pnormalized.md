---
uid: Microsoft.Quantum.Math.PNormalized
title: De functie PNormalized
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854837"
---
# <a name="pnormalized-function"></a><span data-ttu-id="c816c-102">De functie PNormalized</span><span class="sxs-lookup"><span data-stu-id="c816c-102">PNormalized function</span></span>

<span data-ttu-id="c816c-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="c816c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="c816c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c816c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c816c-105">Normaliseert een vector van `Double` s in de `L(p)` norm.</span><span class="sxs-lookup"><span data-stu-id="c816c-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="c816c-106">Op basis van een matrix $x $ van type, wordt hiermee `Double[]` een matrix geretourneerd waarin alle elementen worden gedeeld door de $p $-norm $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="c816c-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="c816c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c816c-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="c816c-108">p: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c816c-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c816c-109">De exponent $p $ in de $p $-norm.</span><span class="sxs-lookup"><span data-stu-id="c816c-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="c816c-110">matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c816c-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="c816c-111">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c816c-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c816c-112">De matrix $x $ genormaliseerd door de $p $-norm $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="c816c-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="c816c-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c816c-113">See Also</span></span>

- [<span data-ttu-id="c816c-114">Micro soft. Quantum. math. PNorm</span><span class="sxs-lookup"><span data-stu-id="c816c-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)