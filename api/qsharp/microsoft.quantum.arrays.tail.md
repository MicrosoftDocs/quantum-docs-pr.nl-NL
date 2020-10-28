---
uid: Microsoft.Quantum.Arrays.Tail
title: Functie staart
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 7a1eb2afefd662f90e58798b56bc83b34ac2abfd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705741"
---
# <a name="tail-function"></a><span data-ttu-id="22cf5-102">Functie staart</span><span class="sxs-lookup"><span data-stu-id="22cf5-102">Tail function</span></span>

<span data-ttu-id="22cf5-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="22cf5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="22cf5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="22cf5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="22cf5-105">Retourneert het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="22cf5-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="22cf5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="22cf5-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="22cf5-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="22cf5-107">array : 'A[]</span></span>

<span data-ttu-id="22cf5-108">De matrix waarvan het laatste element is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22cf5-108">Array of which the last element is taken.</span></span> <span data-ttu-id="22cf5-109">De matrix moet een lengte van ten minste 1 hebben.</span><span class="sxs-lookup"><span data-stu-id="22cf5-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="22cf5-110">Uitvoer: ' A</span><span class="sxs-lookup"><span data-stu-id="22cf5-110">Output : 'A</span></span>

<span data-ttu-id="22cf5-111">Het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="22cf5-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="22cf5-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="22cf5-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="22cf5-113">' A</span><span class="sxs-lookup"><span data-stu-id="22cf5-113">'A</span></span>

<span data-ttu-id="22cf5-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="22cf5-114">The type of the array elements.</span></span>