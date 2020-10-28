---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: De functie HeadAndRest
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705981"
---
# <a name="headandrest-function"></a><span data-ttu-id="7e916-102">De functie HeadAndRest</span><span class="sxs-lookup"><span data-stu-id="7e916-102">HeadAndRest function</span></span>

<span data-ttu-id="7e916-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7e916-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7e916-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e916-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e916-105">Retourneert een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="7e916-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="7e916-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7e916-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="7e916-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="7e916-107">array : 'A[]</span></span>

<span data-ttu-id="7e916-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="7e916-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="7e916-109">Uitvoer: (' A ', ' A [])</span><span class="sxs-lookup"><span data-stu-id="7e916-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="7e916-110">Een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="7e916-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7e916-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7e916-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="7e916-112">' A</span><span class="sxs-lookup"><span data-stu-id="7e916-112">'A</span></span>

<span data-ttu-id="7e916-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="7e916-113">The type of the array elements.</span></span>