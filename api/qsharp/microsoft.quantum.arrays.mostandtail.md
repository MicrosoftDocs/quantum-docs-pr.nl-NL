---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: De functie MostAndTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845593"
---
# <a name="mostandtail-function"></a><span data-ttu-id="476b3-102">De functie MostAndTail</span><span class="sxs-lookup"><span data-stu-id="476b3-102">MostAndTail function</span></span>

<span data-ttu-id="476b3-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="476b3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="476b3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="476b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="476b3-105">Retourneert een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="476b3-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="476b3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="476b3-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="476b3-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="476b3-107">array : 'A[]</span></span>

<span data-ttu-id="476b3-108">Een matrix met ten minste één element.</span><span class="sxs-lookup"><span data-stu-id="476b3-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="476b3-109">Output: (' A [], ' A)</span><span class="sxs-lookup"><span data-stu-id="476b3-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="476b3-110">Een tuple van alle, maar één en het laatste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="476b3-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="476b3-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="476b3-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="476b3-112">' A</span><span class="sxs-lookup"><span data-stu-id="476b3-112">'A</span></span>

<span data-ttu-id="476b3-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="476b3-113">The type of the array elements.</span></span>