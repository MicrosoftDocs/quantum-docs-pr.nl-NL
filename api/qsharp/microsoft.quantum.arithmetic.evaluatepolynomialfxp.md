---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Bewerking EvaluatePolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707317"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="bba2d-102">Bewerking EvaluatePolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="bba2d-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="bba2d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="bba2d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="bba2d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bba2d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bba2d-105">Evalueert een polynoom in een vaste-komma weergave.</span><span class="sxs-lookup"><span data-stu-id="bba2d-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="bba2d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bba2d-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="bba2d-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bba2d-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bba2d-108">Coëfficiënten van de polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_d] $ voor de polynomiale $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="bba2d-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="bba2d-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="bba2d-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="bba2d-110">Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="bba2d-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="bba2d-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="bba2d-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="bba2d-112">Het vaste-komma nummer van de uitvoer dat $P (x) $ bevat.</span><span class="sxs-lookup"><span data-stu-id="bba2d-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="bba2d-113">Moet in eerste instantie de status $ \ket {0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="bba2d-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bba2d-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bba2d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

