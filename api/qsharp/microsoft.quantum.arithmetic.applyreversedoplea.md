---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA
title: Bewerking ApplyReversedOpLEA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: d5bc1b38500c449b58f8dafd640627b8e933e902
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202733"
---
# <a name="applyreversedoplea-operation"></a><span data-ttu-id="babc1-102">Bewerking ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="babc1-102">ApplyReversedOpLEA operation</span></span>

<span data-ttu-id="babc1-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="babc1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="babc1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="babc1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="babc1-105">Hiermee wordt een bewerking toegepast waarbij invoer van een geringe endian wordt gebruikt voor een registratie die een niet-ondertekend geheel getal versleutelt met de indeling big endian.</span><span class="sxs-lookup"><span data-stu-id="babc1-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="babc1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="babc1-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="babc1-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="babc1-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="babc1-108">Bewerking die wordt uitgevoerd op een little-endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="babc1-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="babc1-109">registreren: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="babc1-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="babc1-110">Een big-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="babc1-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="babc1-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="babc1-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="babc1-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="babc1-112">See Also</span></span>

- [<span data-ttu-id="babc1-113">Micro soft. Quantum. aritmetische. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="babc1-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="babc1-114">Micro soft. Quantum. aritmetische. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="babc1-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="babc1-115">Micro soft. Quantum. aritmetische. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="babc1-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)