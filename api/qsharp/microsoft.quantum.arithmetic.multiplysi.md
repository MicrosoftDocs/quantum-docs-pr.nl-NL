---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Bewerking MultiplySI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7c7e7dfaee9b9dc717db44956506984e60281dd2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843015"
---
# <a name="multiplysi-operation"></a><span data-ttu-id="97845-102">Bewerking MultiplySI</span><span class="sxs-lookup"><span data-stu-id="97845-102">MultiplySI operation</span></span>

<span data-ttu-id="97845-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="97845-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="97845-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="97845-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="97845-105">Vermenigvuldig ondertekend geheel getal `xs` met ondertekende integer `ys` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="97845-105">Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="97845-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="97845-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="97845-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="97845-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="97845-108">n-bits multiplicand (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="97845-108">n-bit multiplicand (SignedLittleEndian)</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="97845-109">kalenderda: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="97845-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="97845-110">n-bits vermenigvuldiger (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="97845-110">n-bit multiplier (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="97845-111">resultaat: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="97845-111">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="97845-112">2n-bit result (SignedLittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="97845-112">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97845-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97845-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

