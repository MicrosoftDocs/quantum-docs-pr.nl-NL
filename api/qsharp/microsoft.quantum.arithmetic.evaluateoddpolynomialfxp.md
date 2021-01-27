---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Bewerking EvaluateOddPolynomialFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 852e986cd09c3b2e31263f53e381d9da73298415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846665"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="9a2ea-102">Bewerking EvaluateOddPolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="9a2ea-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="9a2ea-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9a2ea-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9a2ea-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="9a2ea-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="9a2ea-105">Evalueert een oneven polynoom in een vaste-komma weergave.</span><span class="sxs-lookup"><span data-stu-id="9a2ea-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9a2ea-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9a2ea-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="9a2ea-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9a2ea-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9a2ea-108">Coëfficiënten van de oneven polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_k] $ voor de oneven polynoom $P (x) = a_0 x + a_1 x ^ 3 + \cdots + a_k x ^ {2.000 + 1} $.</span><span class="sxs-lookup"><span data-stu-id="9a2ea-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="9a2ea-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9a2ea-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9a2ea-110">Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="9a2ea-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="9a2ea-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9a2ea-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9a2ea-112">Uitvoer met een vast punt dat P (x) zal bevatten.</span><span class="sxs-lookup"><span data-stu-id="9a2ea-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="9a2ea-113">Moet in eerste instantie de status $ \ket {0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="9a2ea-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a2ea-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a2ea-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

