---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: De functie ReversedOpLEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 2dc6a596970f909af9c329dbe7002c165854cfec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846382"
---
# <a name="reversedoplec-function"></a><span data-ttu-id="f782c-102">De functie ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="f782c-102">ReversedOpLEC function</span></span>

<span data-ttu-id="f782c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f782c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f782c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f782c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f782c-105">Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f782c-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="f782c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f782c-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="f782c-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="f782c-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f782c-108">De bewerking waarvan de invoer moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="f782c-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-ctl"></a><span data-ttu-id="f782c-109">Output: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="f782c-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f782c-110">Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f782c-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="f782c-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f782c-111">See Also</span></span>

- [<span data-ttu-id="f782c-112">Micro soft. Quantum. aritmetische. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="f782c-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="f782c-113">Micro soft. Quantum. aritmetische. ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="f782c-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="f782c-114">Micro soft. Quantum. aritmetische. ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="f782c-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="f782c-115">Micro soft. Quantum. aritmetische. ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="f782c-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)