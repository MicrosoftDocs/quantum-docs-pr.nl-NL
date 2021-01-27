---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: De functie IntegerBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855407"
---
# <a name="integerbits-function"></a><span data-ttu-id="9b250-102">De functie IntegerBits</span><span class="sxs-lookup"><span data-stu-id="9b250-102">IntegerBits function</span></span>

<span data-ttu-id="9b250-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="9b250-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="9b250-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b250-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b250-105">Retourneert alle posities waarin bits van een geheel getal zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9b250-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="9b250-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9b250-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="9b250-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b250-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b250-108">Een niet-negatief getal.</span><span class="sxs-lookup"><span data-stu-id="9b250-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="9b250-109">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b250-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b250-110">Het aantal bits in de binaire uitbrei ding van `value` .</span><span class="sxs-lookup"><span data-stu-id="9b250-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="9b250-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9b250-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9b250-112">Een matrix met alle bits-posities (vanaf 0) die 1 zijn in de binaire uitbrei ding van het `value` overwegen van alle bits tot stand te brengen `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="9b250-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="9b250-113">Alle posities worden in de matrix gesorteerd op positie in een oplopende volg orde.</span><span class="sxs-lookup"><span data-stu-id="9b250-113">All positions are ordered in the array by position in an increasing order.</span></span>

## <a name="example"></a><span data-ttu-id="9b250-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9b250-114">Example</span></span>

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```