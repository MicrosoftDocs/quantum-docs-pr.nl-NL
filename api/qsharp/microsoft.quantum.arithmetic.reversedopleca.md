---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: De functie ReversedOpLECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d4245437f2b71abb8bf1bbe4db43ae7d2ee23799
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845752"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="2cdd3-102">De functie ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="2cdd3-102">ReversedOpLECA function</span></span>

<span data-ttu-id="2cdd3-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2cdd3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2cdd3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2cdd3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2cdd3-105">Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="2cdd3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2cdd3-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="2cdd3-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="2cdd3-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2cdd3-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="2cdd3-109">Uitvoer: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="2cdd3-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2cdd3-110">Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cdd3-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2cdd3-111">See Also</span></span>

- [<span data-ttu-id="2cdd3-112">Micro soft. Quantum. aritmetische. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="2cdd3-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="2cdd3-113">Micro soft. Quantum. aritmetische. ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="2cdd3-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="2cdd3-114">Micro soft. Quantum. aritmetische. ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="2cdd3-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="2cdd3-115">Micro soft. Quantum. aritmetische. ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="2cdd3-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)