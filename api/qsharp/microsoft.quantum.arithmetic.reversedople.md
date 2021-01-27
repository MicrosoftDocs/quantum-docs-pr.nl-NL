---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: De functie ReversedOpLE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d02817e5372b841f3ab633cafa22af603c5310c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846394"
---
# <a name="reversedople-function"></a><span data-ttu-id="02c17-102">De functie ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="02c17-102">ReversedOpLE function</span></span>

<span data-ttu-id="02c17-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="02c17-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="02c17-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02c17-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02c17-105">Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="02c17-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="02c17-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="02c17-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="02c17-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02c17-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="02c17-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="02c17-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit"></a><span data-ttu-id="02c17-109">Uitvoer: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02c17-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="02c17-110">Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="02c17-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="02c17-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="02c17-111">See Also</span></span>

- [<span data-ttu-id="02c17-112">Micro soft. Quantum. aritmetische. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="02c17-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="02c17-113">Micro soft. Quantum. aritmetische. ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="02c17-113">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="02c17-114">Micro soft. Quantum. aritmetische. ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="02c17-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="02c17-115">Micro soft. Quantum. aritmetische. ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="02c17-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)