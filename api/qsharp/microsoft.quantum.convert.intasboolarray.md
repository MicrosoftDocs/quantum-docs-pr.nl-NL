---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: De functie IntAsBoolArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702962"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="e4ea8-102">De functie IntAsBoolArray</span><span class="sxs-lookup"><span data-stu-id="e4ea8-102">IntAsBoolArray function</span></span>

<span data-ttu-id="e4ea8-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="e4ea8-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="e4ea8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e4ea8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e4ea8-105">Produceert een binaire weer gave van een positief geheel getal, met behulp van de weer gave van de little-endian voor de geretourneerde matrix.</span><span class="sxs-lookup"><span data-stu-id="e4ea8-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="e4ea8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e4ea8-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="e4ea8-107">getal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4ea8-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4ea8-108">Een positief geheel getal dat moet worden geconverteerd naar een matrix met Boole-waarden.</span><span class="sxs-lookup"><span data-stu-id="e4ea8-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="e4ea8-109">bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4ea8-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4ea8-110">Het aantal bits in de binaire weer gave van `number` .</span><span class="sxs-lookup"><span data-stu-id="e4ea8-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e4ea8-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e4ea8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e4ea8-112">Een matrix met Boole-waarden die aangeeft `number` .</span><span class="sxs-lookup"><span data-stu-id="e4ea8-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ea8-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e4ea8-113">Remarks</span></span>

<span data-ttu-id="e4ea8-114">De invoer `bits` moet tussen 0 en 63.</span><span class="sxs-lookup"><span data-stu-id="e4ea8-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="e4ea8-115">De invoer `number` moet liggen tussen 0 en $2 ^ {\texttt{bits}}-$1.</span><span class="sxs-lookup"><span data-stu-id="e4ea8-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>