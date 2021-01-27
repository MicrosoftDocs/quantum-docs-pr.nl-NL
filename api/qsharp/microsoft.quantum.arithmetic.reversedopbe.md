---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: De functie ReversedOpBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846487"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="5b4c4-102">De functie ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="5b4c4-102">ReversedOpBE function</span></span>

<span data-ttu-id="5b4c4-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5b4c4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5b4c4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b4c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b4c4-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="5b4c4-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="5b4c4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b4c4-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="5b4c4-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b4c4-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5b4c4-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="5b4c4-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="5b4c4-109">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b4c4-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5b4c4-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="5b4c4-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b4c4-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5b4c4-111">See Also</span></span>

- [<span data-ttu-id="5b4c4-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="5b4c4-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="5b4c4-113">Micro soft. Quantum. aritmetische. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="5b4c4-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="5b4c4-114">Micro soft. Quantum. aritmetische. ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="5b4c4-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="5b4c4-115">Micro soft. Quantum. aritmetische. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="5b4c4-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)