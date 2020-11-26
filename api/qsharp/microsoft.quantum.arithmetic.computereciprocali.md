---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Bewerking ComputeReciprocalI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: 9024da4a457265c65a41ef681cfbb99ebd4989a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223354"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="3ab09-102">Bewerking ComputeReciprocalI</span><span class="sxs-lookup"><span data-stu-id="3ab09-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="3ab09-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3ab09-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3ab09-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="3ab09-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="3ab09-105">Hiermee wordt de reciproque waarde van 1/x voor een niet-ondertekende integer x berekend op basis van de deling van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="3ab09-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="3ab09-106">Het resultaat, geïnterpreteerd als een geheel getal, is `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="3ab09-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3ab09-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ab09-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="3ab09-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ab09-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ab09-109">n-bits geheel getal zonder teken</span><span class="sxs-lookup"><span data-stu-id="3ab09-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="3ab09-110">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ab09-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ab09-111">2n-bits uitvoer moet in $ \ket $ in {0} eerste instantie zijn.</span><span class="sxs-lookup"><span data-stu-id="3ab09-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ab09-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ab09-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ab09-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3ab09-113">Remarks</span></span>

<span data-ttu-id="3ab09-114">Voor de invoer x = 0 is de uitvoer allemaal.</span><span class="sxs-lookup"><span data-stu-id="3ab09-114">For the input x=0, the output will be all-ones.</span></span>