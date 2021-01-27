---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: De functie ReversedOpLEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b0fcf1c735bb19308a381307e64314d9d961e5da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846433"
---
# <a name="reversedoplea-function"></a><span data-ttu-id="d362d-102">De functie ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="d362d-102">ReversedOpLEA function</span></span>

<span data-ttu-id="d362d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d362d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d362d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d362d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d362d-105">Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d362d-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="d362d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d362d-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="d362d-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="d362d-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d362d-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="d362d-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj"></a><span data-ttu-id="d362d-109">Uitvoer: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="d362d-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d362d-110">Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="d362d-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="d362d-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d362d-111">See Also</span></span>

- [<span data-ttu-id="d362d-112">Micro soft. Quantum. aritmetische. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="d362d-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="d362d-113">Micro soft. Quantum. aritmetische. ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="d362d-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="d362d-114">Micro soft. Quantum. aritmetische. ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="d362d-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="d362d-115">Micro soft. Quantum. aritmetische. ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="d362d-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)