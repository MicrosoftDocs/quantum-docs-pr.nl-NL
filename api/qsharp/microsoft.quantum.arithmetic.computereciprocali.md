---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Bewerking ComputeReciprocalI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: b99e816ed69af6e6d1758442d6f95c5ab0e5c07a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707348"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="7a6ec-102">Bewerking ComputeReciprocalI</span><span class="sxs-lookup"><span data-stu-id="7a6ec-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="7a6ec-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7a6ec-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7a6ec-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7a6ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7a6ec-105">Hiermee wordt de reciproque waarde van 1/x voor een niet-ondertekende integer x berekend op basis van de deling van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="7a6ec-106">Het resultaat, geïnterpreteerd als een geheel getal, is `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="7a6ec-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="7a6ec-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="7a6ec-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7a6ec-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7a6ec-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7a6ec-109">n-bits geheel getal zonder teken</span><span class="sxs-lookup"><span data-stu-id="7a6ec-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="7a6ec-110">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7a6ec-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7a6ec-111">2n-bits uitvoer moet in $ \ket $ in {0} eerste instantie zijn.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7a6ec-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7a6ec-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7a6ec-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7a6ec-113">Remarks</span></span>

<span data-ttu-id="7a6ec-114">Voor de invoer x = 0 is de uitvoer allemaal.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-114">For the input x=0, the output will be all-ones.</span></span>