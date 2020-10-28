---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA
title: Bewerking ApplyReversedOpBEA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: f606011dd002d6eadc4f882005f4577aeb28cac0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707517"
---
# <a name="applyreversedopbea-operation"></a><span data-ttu-id="dbf93-102">Bewerking ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="dbf93-102">ApplyReversedOpBEA operation</span></span>

<span data-ttu-id="dbf93-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dbf93-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dbf93-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dbf93-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dbf93-105">Past een bewerking die invoer van big endian in een REGI ster versleutelt, een niet-ondertekend geheel getal met de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="dbf93-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="dbf93-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dbf93-106">Input</span></span>

### <a name="op--bigendian--unit-adj"></a><span data-ttu-id="dbf93-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="dbf93-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="dbf93-108">Bewerking die op een big endian-REGI ster werkt.</span><span class="sxs-lookup"><span data-stu-id="dbf93-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="dbf93-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dbf93-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dbf93-110">Een little-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="dbf93-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dbf93-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dbf93-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="dbf93-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dbf93-112">See Also</span></span>

- [<span data-ttu-id="dbf93-113">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="dbf93-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="dbf93-114">Micro soft. Quantum. aritmetische. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="dbf93-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="dbf93-115">Micro soft. Quantum. aritmetische. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="dbf93-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)