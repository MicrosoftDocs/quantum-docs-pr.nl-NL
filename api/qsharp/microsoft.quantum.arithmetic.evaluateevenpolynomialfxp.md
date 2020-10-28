---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Bewerking EvaluateEvenPolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: e49a6d47553a60766b561525e8cfa37e95fda9e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707332"
---
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="a4328-102">Bewerking EvaluateEvenPolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="a4328-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="a4328-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a4328-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a4328-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4328-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4328-105">Hiermee wordt een gelijkmatige polynoom geëvalueerd in een vaste-komma weergave.</span><span class="sxs-lookup"><span data-stu-id="a4328-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="a4328-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a4328-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a4328-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a4328-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a4328-108">Coëfficiënten van de zelfs polynoom als een dubbele matrix, dat wil zeggen: de matrix $ [a_0, a_1,..., a_k] $ voor de even polynomiale $P (x) = a_0 + a_1 x ^ 2 + \cdots + a_k x ^ {2.000} $.</span><span class="sxs-lookup"><span data-stu-id="a4328-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="a4328-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a4328-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a4328-110">Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="a4328-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="a4328-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a4328-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a4328-112">Het vaste-komma nummer van de uitvoer dat $P (x) $ bevat.</span><span class="sxs-lookup"><span data-stu-id="a4328-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="a4328-113">Moet in eerste instantie de status $ \ket {0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="a4328-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4328-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4328-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

