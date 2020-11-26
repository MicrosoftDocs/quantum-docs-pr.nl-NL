---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: De functie HeadAndRest
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221076"
---
# <a name="headandrest-function"></a><span data-ttu-id="e9b6c-102">De functie HeadAndRest</span><span class="sxs-lookup"><span data-stu-id="e9b6c-102">HeadAndRest function</span></span>

<span data-ttu-id="e9b6c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e9b6c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e9b6c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9b6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9b6c-105">Retourneert een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="e9b6c-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="e9b6c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e9b6c-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="e9b6c-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="e9b6c-107">array : 'A[]</span></span>

<span data-ttu-id="e9b6c-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="e9b6c-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="e9b6c-109">Uitvoer: (' A ', ' A [])</span><span class="sxs-lookup"><span data-stu-id="e9b6c-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="e9b6c-110">Een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="e9b6c-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e9b6c-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e9b6c-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="e9b6c-112">' A</span><span class="sxs-lookup"><span data-stu-id="e9b6c-112">'A</span></span>

<span data-ttu-id="e9b6c-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="e9b6c-113">The type of the array elements.</span></span>