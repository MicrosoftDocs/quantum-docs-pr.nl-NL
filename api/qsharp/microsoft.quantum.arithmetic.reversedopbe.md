---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: De functie ReversedOpBE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 170f63e60e6c26dbdd33af02c6a3387a1b3dbc44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706332"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="e5159-102">De functie ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="e5159-102">ReversedOpBE function</span></span>

<span data-ttu-id="e5159-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e5159-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e5159-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5159-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5159-105">Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e5159-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="e5159-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e5159-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="e5159-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5159-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e5159-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="e5159-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="e5159-109">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5159-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e5159-110">Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.</span><span class="sxs-lookup"><span data-stu-id="e5159-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5159-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e5159-111">See Also</span></span>

- [<span data-ttu-id="e5159-112">Micro soft. Quantum. aritmetische. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="e5159-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="e5159-113">Micro soft. Quantum. aritmetische. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="e5159-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="e5159-114">Micro soft. Quantum. aritmetische. ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="e5159-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="e5159-115">Micro soft. Quantum. aritmetische. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="e5159-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)