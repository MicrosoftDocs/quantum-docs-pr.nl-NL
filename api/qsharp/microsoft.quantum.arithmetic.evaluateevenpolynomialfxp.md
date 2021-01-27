---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Bewerking EvaluateEvenPolynomialFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: c3129cb796a344f7ad38a585183db285d48892bf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843235"
---
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="ebc82-102">Bewerking EvaluateEvenPolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="ebc82-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="ebc82-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ebc82-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ebc82-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="ebc82-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="ebc82-105">Hiermee wordt een gelijkmatige polynoom geëvalueerd in een vaste-komma weergave.</span><span class="sxs-lookup"><span data-stu-id="ebc82-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ebc82-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ebc82-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="ebc82-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ebc82-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ebc82-108">Coëfficiënten van de zelfs polynoom als een dubbele matrix, dat wil zeggen: de matrix $ [a_0, a_1,..., a_k] $ voor de even polynomiale $P (x) = a_0 + a_1 x ^ 2 + \cdots + a_k x ^ {2.000} $.</span><span class="sxs-lookup"><span data-stu-id="ebc82-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="ebc82-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ebc82-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ebc82-110">Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="ebc82-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="ebc82-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ebc82-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ebc82-112">Het vaste-komma nummer van de uitvoer dat $P (x) $ bevat.</span><span class="sxs-lookup"><span data-stu-id="ebc82-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="ebc82-113">Moet in eerste instantie de status $ \ket {0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="ebc82-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ebc82-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ebc82-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

