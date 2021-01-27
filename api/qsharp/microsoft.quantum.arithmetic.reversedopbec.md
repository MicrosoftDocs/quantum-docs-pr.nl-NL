---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: De functie ReversedOpBEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 0674567f5d45890aa2f631b2e0e4d75d20a72449
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846441"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="7033f-102">De functie ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="7033f-102">ReversedOpBEC function</span></span>

<span data-ttu-id="7033f-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7033f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7033f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7033f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7033f-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="7033f-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="7033f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7033f-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="7033f-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="7033f-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7033f-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="7033f-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-ctl"></a><span data-ttu-id="7033f-109">Output: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="7033f-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7033f-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="7033f-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="7033f-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7033f-111">See Also</span></span>

- [<span data-ttu-id="7033f-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="7033f-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="7033f-113">Micro soft. Quantum. aritmetische. ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="7033f-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="7033f-114">Micro soft. Quantum. aritmetische. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="7033f-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="7033f-115">Micro soft. Quantum. aritmetische. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="7033f-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)