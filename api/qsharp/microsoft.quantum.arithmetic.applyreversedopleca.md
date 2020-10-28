---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA
title: Bewerking ApplyReversedOpLECA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLECA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 6e4edd30e33be1a8039b7fd6551470abee26ea27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707477"
---
# <a name="applyreversedopleca-operation"></a><span data-ttu-id="11a51-102">Bewerking ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="11a51-102">ApplyReversedOpLECA operation</span></span>

<span data-ttu-id="11a51-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="11a51-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="11a51-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="11a51-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="11a51-105">Hiermee wordt een bewerking toegepast waarbij invoer van een geringe endian wordt gebruikt voor een registratie die een niet-ondertekend geheel getal versleutelt met de indeling big endian.</span><span class="sxs-lookup"><span data-stu-id="11a51-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="11a51-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="11a51-106">Input</span></span>

### <a name="op--littleendian--unit-ctl--adj"></a><span data-ttu-id="11a51-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="11a51-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="11a51-108">Bewerking die wordt uitgevoerd op een little-endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="11a51-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="11a51-109">registreren: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="11a51-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="11a51-110">Een big-endian-registratie die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="11a51-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="11a51-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11a51-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="11a51-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="11a51-112">See Also</span></span>

- [<span data-ttu-id="11a51-113">Micro soft. Quantum. aritmetische. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="11a51-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="11a51-114">Micro soft. Quantum. aritmetische. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="11a51-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="11a51-115">Micro soft. Quantum. aritmetische. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="11a51-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)