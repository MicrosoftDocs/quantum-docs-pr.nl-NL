---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Bewerking SquareSI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: c8c4e3cca001aa6d7ce1b9df106ce77f74524301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706220"
---
# <a name="squaresi-operation"></a><span data-ttu-id="464d5-102">Bewerking SquareSI</span><span class="sxs-lookup"><span data-stu-id="464d5-102">SquareSI operation</span></span>

<span data-ttu-id="464d5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="464d5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="464d5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="464d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="464d5-105">Vier kant ondertekend geheel getal `xs` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="464d5-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="464d5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="464d5-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="464d5-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="464d5-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="464d5-108">n-bits geheel getal naar vier kant (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="464d5-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="464d5-109">resultaat: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="464d5-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="464d5-110">2n-bit result (SignedLittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="464d5-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="464d5-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="464d5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="464d5-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="464d5-112">Remarks</span></span>

<span data-ttu-id="464d5-113">De implementatie is afhankelijk van IntegerSquare.</span><span class="sxs-lookup"><span data-stu-id="464d5-113">The implementation relies on IntegerSquare.</span></span>