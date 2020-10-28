---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: Bewerking ApplyReversedOpLE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 0f73ac7d50e32f4467bc1683e421149fa38ee29a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707501"
---
# <a name="applyreversedople-operation"></a><span data-ttu-id="ddcb3-102">Bewerking ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="ddcb3-102">ApplyReversedOpLE operation</span></span>

<span data-ttu-id="ddcb3-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ddcb3-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ddcb3-105">Hiermee wordt een bewerking toegepast waarbij invoer van een geringe endian wordt gebruikt voor een registratie die een niet-ondertekend geheel getal versleutelt met de indeling big endian.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ddcb3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ddcb3-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="ddcb3-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ddcb3-108">Bewerking die wordt uitgevoerd op een little-endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="ddcb3-109">registreren: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="ddcb3-110">Een big-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ddcb3-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ddcb3-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ddcb3-112">See Also</span></span>

- [<span data-ttu-id="ddcb3-113">Micro soft. Quantum. aritmetische. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="ddcb3-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="ddcb3-114">Micro soft. Quantum. aritmetische. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="ddcb3-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="ddcb3-115">Micro soft. Quantum. aritmetische. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="ddcb3-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)