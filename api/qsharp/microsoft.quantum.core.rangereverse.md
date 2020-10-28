---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702866"
---
# <a name="rangereverse-function"></a><span data-ttu-id="e6a43-102">De functie RangeReverse</span><span class="sxs-lookup"><span data-stu-id="e6a43-102">RangeReverse function</span></span>

<span data-ttu-id="e6a43-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e6a43-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e6a43-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6a43-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6a43-105">Retourneert een nieuw bereik dat het omgekeerde is van het invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="e6a43-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="e6a43-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e6a43-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="e6a43-107">r: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e6a43-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="e6a43-108">Invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="e6a43-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="e6a43-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e6a43-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="e6a43-110">Een nieuw bereik dat het omgekeerde is van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="e6a43-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a43-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e6a43-111">Remarks</span></span>

<span data-ttu-id="e6a43-112">Houd er rekening mee dat het omgekeerde van een bereik niet gewoon `end` .. `-step` .. is `start` , omdat het daad werkelijke laatste element van een bereik mogelijk niet hetzelfde is als `end` .</span><span class="sxs-lookup"><span data-stu-id="e6a43-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>