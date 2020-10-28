---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: De functie MostAndTail
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 8786250cf2f78ce2e9ff8baddc856d0bc07cb9a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705860"
---
# <a name="mostandtail-function"></a><span data-ttu-id="6ae64-102">De functie MostAndTail</span><span class="sxs-lookup"><span data-stu-id="6ae64-102">MostAndTail function</span></span>

<span data-ttu-id="6ae64-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6ae64-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6ae64-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6ae64-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6ae64-105">Retourneert een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="6ae64-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="6ae64-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6ae64-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="6ae64-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="6ae64-107">array : 'A[]</span></span>

<span data-ttu-id="6ae64-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="6ae64-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="6ae64-109">Output: (' A [], ' A)</span><span class="sxs-lookup"><span data-stu-id="6ae64-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="6ae64-110">Een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="6ae64-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6ae64-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6ae64-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="6ae64-112">' A</span><span class="sxs-lookup"><span data-stu-id="6ae64-112">'A</span></span>

<span data-ttu-id="6ae64-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="6ae64-113">The type of the array elements.</span></span>