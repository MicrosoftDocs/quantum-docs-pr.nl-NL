---
uid: Microsoft.Quantum.Math.PNorm
title: De functie PNorm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: cea85715e448305486f6d8a6c10e11da56edf3ee
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707921"
---
# <a name="pnorm-function"></a><span data-ttu-id="a16cd-102">De functie PNorm</span><span class="sxs-lookup"><span data-stu-id="a16cd-102">PNorm function</span></span>

<span data-ttu-id="a16cd-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a16cd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a16cd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a16cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a16cd-105">Retourneert de `L(p)` norm van een vector van `Double` s.</span><span class="sxs-lookup"><span data-stu-id="a16cd-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="a16cd-106">Op basis van een matrix $x $ van het type `Double[]` , retourneert dit de $p $-norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.</span><span class="sxs-lookup"><span data-stu-id="a16cd-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="a16cd-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="a16cd-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="a16cd-108">p: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a16cd-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a16cd-109">De exponent $p $ in de $p $-norm.</span><span class="sxs-lookup"><span data-stu-id="a16cd-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="a16cd-110">matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a16cd-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="a16cd-111">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a16cd-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a16cd-112">De $p $-norm $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="a16cd-112">The $p$-norm $\|x\|_p$.</span></span>