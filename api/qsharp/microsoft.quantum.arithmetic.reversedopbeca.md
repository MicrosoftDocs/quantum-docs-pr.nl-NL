---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: De functie ReversedOpBECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 09bb99645d5946af0e0c654500165077691f8da3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846416"
---
# <a name="reversedopbeca-function"></a><span data-ttu-id="640ad-102">De functie ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="640ad-102">ReversedOpBECA function</span></span>

<span data-ttu-id="640ad-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="640ad-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="640ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="640ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="640ad-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="640ad-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="640ad-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="640ad-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="640ad-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="640ad-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="640ad-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="640ad-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="640ad-109">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="640ad-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="640ad-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="640ad-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="640ad-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="640ad-111">See Also</span></span>

- [<span data-ttu-id="640ad-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="640ad-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [<span data-ttu-id="640ad-113">Micro soft. Quantum. aritmetische. ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="640ad-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="640ad-114">Micro soft. Quantum. aritmetische. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="640ad-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="640ad-115">Micro soft. Quantum. aritmetische. ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="640ad-115">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)