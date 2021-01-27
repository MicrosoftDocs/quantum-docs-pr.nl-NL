---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: De functie ReversedOpBEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 392b97171bcfb9d35a38189fc9c27e61cf9cf7d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846457"
---
# <a name="reversedopbea-function"></a><span data-ttu-id="c7415-102">De functie ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="c7415-102">ReversedOpBEA function</span></span>

<span data-ttu-id="c7415-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c7415-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c7415-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7415-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7415-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c7415-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="c7415-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c7415-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="c7415-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c7415-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c7415-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="c7415-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj"></a><span data-ttu-id="c7415-109">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c7415-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c7415-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="c7415-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7415-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c7415-111">See Also</span></span>

- [<span data-ttu-id="c7415-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="c7415-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="c7415-113">Micro soft. Quantum. aritmetische. ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="c7415-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="c7415-114">Micro soft. Quantum. aritmetische. ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="c7415-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="c7415-115">Micro soft. Quantum. aritmetische. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="c7415-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)