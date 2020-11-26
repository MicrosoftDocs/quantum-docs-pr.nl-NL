---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA
title: Bewerking ApplyReversedOpBEA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 17d05e0914eead28ff0e04b858b003659d37ab7f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202818"
---
# <a name="applyreversedopbea-operation"></a><span data-ttu-id="bba13-102">Bewerking ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="bba13-102">ApplyReversedOpBEA operation</span></span>

<span data-ttu-id="bba13-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="bba13-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="bba13-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bba13-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bba13-105">Past een bewerking die invoer van big endian in een REGI ster versleutelt, een niet-ondertekend geheel getal met de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="bba13-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="bba13-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bba13-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="bba13-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="bba13-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bba13-108">Bewerking die op een big endian-REGI ster werkt.</span><span class="sxs-lookup"><span data-stu-id="bba13-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="bba13-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bba13-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bba13-110">Een little-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="bba13-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bba13-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bba13-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bba13-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bba13-112">See Also</span></span>

- [<span data-ttu-id="bba13-113">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="bba13-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="bba13-114">Micro soft. Quantum. aritmetische. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="bba13-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="bba13-115">Micro soft. Quantum. aritmetische. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="bba13-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)