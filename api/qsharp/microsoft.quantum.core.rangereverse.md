---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853646"
---
# <a name="rangereverse-function"></a><span data-ttu-id="f80cd-102">De functie RangeReverse</span><span class="sxs-lookup"><span data-stu-id="f80cd-102">RangeReverse function</span></span>

<span data-ttu-id="f80cd-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="f80cd-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="f80cd-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f80cd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f80cd-105">Retourneert een nieuw bereik dat het omgekeerde is van het invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="f80cd-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="f80cd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f80cd-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="f80cd-107">r: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f80cd-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="f80cd-108">Invoer bereik.</span><span class="sxs-lookup"><span data-stu-id="f80cd-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="f80cd-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f80cd-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="f80cd-110">Een nieuw bereik dat het omgekeerde is van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="f80cd-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="f80cd-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f80cd-111">Remarks</span></span>

<span data-ttu-id="f80cd-112">Houd er rekening mee dat het omgekeerde van een bereik niet gewoon `end` .. `-step` .. is `start` , omdat het daad werkelijke laatste element van een bereik mogelijk niet hetzelfde is als `end` .</span><span class="sxs-lookup"><span data-stu-id="f80cd-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>