---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA
title: Bewerking ApplyReversedOpLECA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLECA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: c0bc04efe55792f5e177266c27552fb0546707e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202580"
---
# <a name="applyreversedopleca-operation"></a><span data-ttu-id="e0448-102">Bewerking ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="e0448-102">ApplyReversedOpLECA operation</span></span>

<span data-ttu-id="e0448-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e0448-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e0448-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0448-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0448-105">Hiermee wordt een bewerking toegepast waarbij invoer van een geringe endian wordt gebruikt voor een registratie die een niet-ondertekend geheel getal versleutelt met de indeling big endian.</span><span class="sxs-lookup"><span data-stu-id="e0448-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e0448-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e0448-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="e0448-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="e0448-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e0448-108">Bewerking die wordt uitgevoerd op een little-endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="e0448-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="e0448-109">registreren: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="e0448-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="e0448-110">Een big-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="e0448-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e0448-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0448-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e0448-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e0448-112">See Also</span></span>

- [<span data-ttu-id="e0448-113">Micro soft. Quantum. aritmetische. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="e0448-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="e0448-114">Micro soft. Quantum. aritmetische. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="e0448-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="e0448-115">Micro soft. Quantum. aritmetische. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="e0448-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)