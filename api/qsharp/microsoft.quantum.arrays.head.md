---
uid: Microsoft.Quantum.Arrays.Head
title: Head-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 834cbe2384122463be6a0efcb6e09785aae9c092
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221110"
---
# <a name="head-function"></a><span data-ttu-id="882a2-102">Head-functie</span><span class="sxs-lookup"><span data-stu-id="882a2-102">Head function</span></span>

<span data-ttu-id="882a2-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="882a2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="882a2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="882a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="882a2-105">Retourneert het eerste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="882a2-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="882a2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="882a2-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="882a2-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="882a2-107">array : 'A[]</span></span>

<span data-ttu-id="882a2-108">De matrix waarvan het eerste element wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="882a2-108">Array of which the first element is taken.</span></span> <span data-ttu-id="882a2-109">De matrix moet een lengte van ten minste 1 hebben.</span><span class="sxs-lookup"><span data-stu-id="882a2-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="882a2-110">Uitvoer: ' A</span><span class="sxs-lookup"><span data-stu-id="882a2-110">Output : 'A</span></span>

<span data-ttu-id="882a2-111">Het eerste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="882a2-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="882a2-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="882a2-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="882a2-113">' A</span><span class="sxs-lookup"><span data-stu-id="882a2-113">'A</span></span>

<span data-ttu-id="882a2-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="882a2-114">The type of the array elements.</span></span>