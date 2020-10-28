---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Bewerking ApplyReversedOpBECA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 1a11b85e4eca627246d7b9d3b4c10824296e9a77
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707509"
---
# <a name="applyreversedopbeca-operation"></a><span data-ttu-id="9bf33-102">Bewerking ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="9bf33-102">ApplyReversedOpBECA operation</span></span>

<span data-ttu-id="9bf33-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9bf33-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9bf33-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9bf33-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9bf33-105">Past een bewerking die invoer van big endian in een REGI ster versleutelt, een niet-ondertekend geheel getal met de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="9bf33-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="9bf33-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9bf33-106">Input</span></span>

### <a name="op--bigendian--unit-ctl--adj"></a><span data-ttu-id="9bf33-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="9bf33-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="9bf33-108">Bewerking die op een big endian-REGI ster werkt.</span><span class="sxs-lookup"><span data-stu-id="9bf33-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="9bf33-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9bf33-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9bf33-110">Een little-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="9bf33-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9bf33-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9bf33-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9bf33-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9bf33-112">See Also</span></span>

- [<span data-ttu-id="9bf33-113">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="9bf33-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="9bf33-114">Micro soft. Quantum. aritmetische. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="9bf33-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="9bf33-115">Micro soft. Quantum. aritmetische. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="9bf33-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)