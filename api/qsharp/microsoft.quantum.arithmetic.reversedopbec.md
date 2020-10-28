---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: De functie ReversedOpBEC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5e9aa6e6dfef74bca004170cf2b1cd91aa13f0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706316"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="d6b06-102">De functie ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="d6b06-102">ReversedOpBEC function</span></span>

<span data-ttu-id="d6b06-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d6b06-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d6b06-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6b06-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6b06-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d6b06-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="d6b06-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d6b06-106">Input</span></span>

### <a name="op--bigendian--unit-ctl"></a><span data-ttu-id="d6b06-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) -CTL</span><span class="sxs-lookup"><span data-stu-id="d6b06-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="d6b06-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="d6b06-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit-ctl"></a><span data-ttu-id="d6b06-109">Uitvoer: CTL van [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d6b06-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="d6b06-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="d6b06-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6b06-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d6b06-111">See Also</span></span>

- [<span data-ttu-id="d6b06-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="d6b06-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="d6b06-113">Micro soft. Quantum. aritmetische. ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="d6b06-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="d6b06-114">Micro soft. Quantum. aritmetische. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="d6b06-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="d6b06-115">Micro soft. Quantum. aritmetische. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="d6b06-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)