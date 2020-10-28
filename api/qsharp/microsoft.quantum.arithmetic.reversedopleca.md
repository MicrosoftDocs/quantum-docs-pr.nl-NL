---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: De functie ReversedOpLECA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b5413e43ad50ba7252705ef53b21e63650dbb2a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706276"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="e9158-102">De functie ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="e9158-102">ReversedOpLECA function</span></span>

<span data-ttu-id="e9158-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e9158-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e9158-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e9158-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e9158-105">Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e9158-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="e9158-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e9158-106">Input</span></span>

### <a name="op--littleendian--unit-adj--ctl"></a><span data-ttu-id="e9158-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e9158-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e9158-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="e9158-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit-adj--ctl"></a><span data-ttu-id="e9158-109">Output: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e9158-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e9158-110">Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e9158-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9158-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e9158-111">See Also</span></span>

- [<span data-ttu-id="e9158-112">Micro soft. Quantum. aritmetische. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="e9158-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="e9158-113">Micro soft. Quantum. aritmetische. ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="e9158-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="e9158-114">Micro soft. Quantum. aritmetische. ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="e9158-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="e9158-115">Micro soft. Quantum. aritmetische. ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="e9158-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)