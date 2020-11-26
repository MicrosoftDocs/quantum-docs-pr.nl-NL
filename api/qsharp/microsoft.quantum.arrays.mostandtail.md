---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: De functie MostAndTail
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220566"
---
# <a name="mostandtail-function"></a><span data-ttu-id="2881e-102">De functie MostAndTail</span><span class="sxs-lookup"><span data-stu-id="2881e-102">MostAndTail function</span></span>

<span data-ttu-id="2881e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2881e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2881e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2881e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2881e-105">Retourneert een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="2881e-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="2881e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2881e-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="2881e-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="2881e-107">array : 'A[]</span></span>

<span data-ttu-id="2881e-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="2881e-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="2881e-109">Output: (' A [], ' A)</span><span class="sxs-lookup"><span data-stu-id="2881e-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="2881e-110">Een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="2881e-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2881e-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2881e-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="2881e-112">' A</span><span class="sxs-lookup"><span data-stu-id="2881e-112">'A</span></span>

<span data-ttu-id="2881e-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="2881e-113">The type of the array elements.</span></span>