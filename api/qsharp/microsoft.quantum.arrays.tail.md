---
uid: Microsoft.Quantum.Arrays.Tail
title: Functie staart
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 7084cd8bc75f295024dce361153b58490074cdc5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220090"
---
# <a name="tail-function"></a><span data-ttu-id="d24e2-102">Functie staart</span><span class="sxs-lookup"><span data-stu-id="d24e2-102">Tail function</span></span>

<span data-ttu-id="d24e2-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d24e2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d24e2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d24e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d24e2-105">Retourneert het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="d24e2-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="d24e2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d24e2-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="d24e2-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="d24e2-107">array : 'A[]</span></span>

<span data-ttu-id="d24e2-108">De matrix waarvan het laatste element is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d24e2-108">Array of which the last element is taken.</span></span> <span data-ttu-id="d24e2-109">De matrix moet een lengte van ten minste 1 hebben.</span><span class="sxs-lookup"><span data-stu-id="d24e2-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="d24e2-110">Uitvoer: ' A</span><span class="sxs-lookup"><span data-stu-id="d24e2-110">Output : 'A</span></span>

<span data-ttu-id="d24e2-111">Het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="d24e2-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d24e2-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d24e2-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="d24e2-113">' A</span><span class="sxs-lookup"><span data-stu-id="d24e2-113">'A</span></span>

<span data-ttu-id="d24e2-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="d24e2-114">The type of the array elements.</span></span>