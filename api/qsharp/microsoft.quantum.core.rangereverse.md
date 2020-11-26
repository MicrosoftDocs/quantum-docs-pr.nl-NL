---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213834"
---
# <a name="rangereverse-function"></a><span data-ttu-id="26624-102">De functie RangeReverse</span><span class="sxs-lookup"><span data-stu-id="26624-102">RangeReverse function</span></span>

<span data-ttu-id="26624-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="26624-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="26624-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="26624-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="26624-105">Retourneert een nieuw bereik dat het omgekeerde is van het invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="26624-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="26624-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="26624-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="26624-107">r: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="26624-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="26624-108">Invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="26624-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="26624-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="26624-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="26624-110">Een nieuw bereik dat het omgekeerde is van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="26624-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="26624-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="26624-111">Remarks</span></span>

<span data-ttu-id="26624-112">Houd er rekening mee dat het omgekeerde van een bereik niet gewoon `end` .. `-step` .. is `start` , omdat het daad werkelijke laatste element van een bereik mogelijk niet hetzelfde is als `end` .</span><span class="sxs-lookup"><span data-stu-id="26624-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>