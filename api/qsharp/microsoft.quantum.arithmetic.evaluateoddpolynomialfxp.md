---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Bewerking EvaluateOddPolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: d52da4092f16d43ab9d08b03f798a4d6789c7348
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707325"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="8f361-102">Bewerking EvaluateOddPolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="8f361-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="8f361-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8f361-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8f361-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8f361-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8f361-105">Evalueert een oneven polynoom in een vaste-komma weergave.</span><span class="sxs-lookup"><span data-stu-id="8f361-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="8f361-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8f361-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="8f361-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8f361-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8f361-108">Coëfficiënten van de oneven polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_k] $ voor de oneven polynoom $P (x) = a_0 x + a_1 x ^ 3 + \cdots + a_k x ^ {2.000 + 1} $.</span><span class="sxs-lookup"><span data-stu-id="8f361-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="8f361-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="8f361-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="8f361-110">Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="8f361-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="8f361-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="8f361-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="8f361-112">Uitvoer met een vast punt dat P (x) zal bevatten.</span><span class="sxs-lookup"><span data-stu-id="8f361-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="8f361-113">Moet in eerste instantie de status $ \ket {0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="8f361-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f361-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f361-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

