---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: Bewerking ApplyReversedOpBEC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 3a5fef3bb4549433540b2a7b5e94d3cd2d527639
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202767"
---
# <a name="applyreversedopbec-operation"></a><span data-ttu-id="81273-102">Bewerking ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="81273-102">ApplyReversedOpBEC operation</span></span>

<span data-ttu-id="81273-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="81273-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="81273-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81273-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81273-105">Past een bewerking die invoer van big endian in een REGI ster versleutelt, een niet-ondertekend geheel getal met de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="81273-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="81273-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="81273-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="81273-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="81273-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="81273-108">Bewerking die op een big endian-REGI ster werkt.</span><span class="sxs-lookup"><span data-stu-id="81273-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="81273-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="81273-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="81273-110">Een little-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="81273-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="81273-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81273-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="81273-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81273-112">See Also</span></span>

- [<span data-ttu-id="81273-113">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="81273-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="81273-114">Micro soft. Quantum. aritmetische. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="81273-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="81273-115">Micro soft. Quantum. aritmetische. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="81273-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)