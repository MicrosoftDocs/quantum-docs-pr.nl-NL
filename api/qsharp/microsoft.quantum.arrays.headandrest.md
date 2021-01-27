---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: De functie HeadAndRest
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848551"
---
# <a name="headandrest-function"></a><span data-ttu-id="557f7-102">De functie HeadAndRest</span><span class="sxs-lookup"><span data-stu-id="557f7-102">HeadAndRest function</span></span>

<span data-ttu-id="557f7-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="557f7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="557f7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="557f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="557f7-105">Retourneert een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="557f7-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="557f7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="557f7-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="557f7-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="557f7-107">array : 'A[]</span></span>

<span data-ttu-id="557f7-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="557f7-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="557f7-109">Uitvoer: (' A ', ' A [])</span><span class="sxs-lookup"><span data-stu-id="557f7-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="557f7-110">Een tuple van de eerste en alle resterende elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="557f7-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="557f7-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="557f7-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="557f7-112">' A</span><span class="sxs-lookup"><span data-stu-id="557f7-112">'A</span></span>

<span data-ttu-id="557f7-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="557f7-113">The type of the array elements.</span></span>