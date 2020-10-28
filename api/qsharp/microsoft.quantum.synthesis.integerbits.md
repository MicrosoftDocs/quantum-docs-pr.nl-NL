---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: De functie IntegerBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706428"
---
# <a name="integerbits-function"></a><span data-ttu-id="1f72f-102">De functie IntegerBits</span><span class="sxs-lookup"><span data-stu-id="1f72f-102">IntegerBits function</span></span>

<span data-ttu-id="1f72f-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1f72f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1f72f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1f72f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1f72f-105">Retourneert alle posities waarin bits van een geheel getal zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1f72f-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="1f72f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1f72f-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="1f72f-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1f72f-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1f72f-108">Een niet-negatief getal.</span><span class="sxs-lookup"><span data-stu-id="1f72f-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="1f72f-109">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1f72f-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1f72f-110">Het aantal bits in de binaire uitbrei ding van `value` .</span><span class="sxs-lookup"><span data-stu-id="1f72f-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="1f72f-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1f72f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1f72f-112">Een matrix met alle bits-posities (vanaf 0) die 1 zijn in de binaire uitbrei ding van het `value` overwegen van alle bits tot stand te brengen `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="1f72f-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="1f72f-113">Alle posities worden in de matrix gesorteerd op positie in een oplopende volg orde.</span><span class="sxs-lookup"><span data-stu-id="1f72f-113">All positions are ordered in the array by position in an increasing order.</span></span>