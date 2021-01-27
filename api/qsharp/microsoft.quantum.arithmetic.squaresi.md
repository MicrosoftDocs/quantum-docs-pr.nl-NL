---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Bewerking SquareSI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 161b45766c6f4d500d25def24aa509ee7fdc8628
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842926"
---
# <a name="squaresi-operation"></a><span data-ttu-id="aecd0-102">Bewerking SquareSI</span><span class="sxs-lookup"><span data-stu-id="aecd0-102">SquareSI operation</span></span>

<span data-ttu-id="aecd0-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aecd0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aecd0-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="aecd0-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="aecd0-105">Vier kant ondertekend geheel getal `xs` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="aecd0-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="aecd0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="aecd0-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="aecd0-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aecd0-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="aecd0-108">n-bits geheel getal naar vier kant (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aecd0-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="aecd0-109">resultaat: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aecd0-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="aecd0-110">2n-bit result (SignedLittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="aecd0-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aecd0-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aecd0-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="aecd0-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="aecd0-112">Remarks</span></span>

<span data-ttu-id="aecd0-113">De implementatie is afhankelijk van IntegerSquare.</span><span class="sxs-lookup"><span data-stu-id="aecd0-113">The implementation relies on IntegerSquare.</span></span>