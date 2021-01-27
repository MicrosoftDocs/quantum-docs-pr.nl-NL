---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: De functie IntAsBoolArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833307"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="0a88b-102">De functie IntAsBoolArray</span><span class="sxs-lookup"><span data-stu-id="0a88b-102">IntAsBoolArray function</span></span>

<span data-ttu-id="0a88b-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="0a88b-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="0a88b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0a88b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0a88b-105">Produceert een binaire weer gave van een niet-negatief geheel getal, met behulp van de weer gave van de little-endian voor de geretourneerde matrix.</span><span class="sxs-lookup"><span data-stu-id="0a88b-105">Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="0a88b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0a88b-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="0a88b-107">getal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0a88b-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0a88b-108">Een niet-negatief geheel getal dat moet worden geconverteerd naar een matrix met Boole-waarden.</span><span class="sxs-lookup"><span data-stu-id="0a88b-108">A non-negative integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="0a88b-109">bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0a88b-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0a88b-110">Het aantal bits in de binaire weer gave van `number` .</span><span class="sxs-lookup"><span data-stu-id="0a88b-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0a88b-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="0a88b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="0a88b-112">Een matrix met Boole-waarden die aangeeft `number` .</span><span class="sxs-lookup"><span data-stu-id="0a88b-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a88b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0a88b-113">Remarks</span></span>

<span data-ttu-id="0a88b-114">De invoer `bits` moet tussen 0 en 63.</span><span class="sxs-lookup"><span data-stu-id="0a88b-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="0a88b-115">De invoer `number` moet liggen tussen 0 en $2 ^ {\texttt{bits}}-$1.</span><span class="sxs-lookup"><span data-stu-id="0a88b-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>