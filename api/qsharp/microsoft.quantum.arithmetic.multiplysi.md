---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Bewerking MultiplySI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 9ca781cbe90a8ec13e6a85a5babaf043bc8f2b5b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706364"
---
# <a name="multiplysi-operation"></a><span data-ttu-id="de6d3-102">Bewerking MultiplySI</span><span class="sxs-lookup"><span data-stu-id="de6d3-102">MultiplySI operation</span></span>

<span data-ttu-id="de6d3-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="de6d3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="de6d3-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="de6d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="de6d3-105">Vermenigvuldig ondertekend geheel getal `xs` met ondertekende integer `ys` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="de6d3-105">Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="de6d3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="de6d3-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="de6d3-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="de6d3-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="de6d3-108">n-bits multiplicand (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="de6d3-108">n-bit multiplicand (SignedLittleEndian)</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="de6d3-109">kalenderda: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="de6d3-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="de6d3-110">n-bits vermenigvuldiger (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="de6d3-110">n-bit multiplier (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="de6d3-111">resultaat: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="de6d3-111">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="de6d3-112">2n-bit result (SignedLittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="de6d3-112">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="de6d3-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="de6d3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

