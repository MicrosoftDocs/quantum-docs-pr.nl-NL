---
uid: Microsoft.Quantum.Arrays.Head
title: Head-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 6dd181914b5ed3ef16a02b31cb6131daf2a34e19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848577"
---
# <a name="head-function"></a><span data-ttu-id="8b337-102">Head-functie</span><span class="sxs-lookup"><span data-stu-id="8b337-102">Head function</span></span>

<span data-ttu-id="8b337-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8b337-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8b337-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b337-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b337-105">Retourneert het eerste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="8b337-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="8b337-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8b337-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="8b337-107">matrix: ' A []</span><span class="sxs-lookup"><span data-stu-id="8b337-107">array : 'A[]</span></span>

<span data-ttu-id="8b337-108">De matrix waarvan het eerste element wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8b337-108">Array of which the first element is taken.</span></span> <span data-ttu-id="8b337-109">De matrix moet een lengte van ten minste 1 hebben.</span><span class="sxs-lookup"><span data-stu-id="8b337-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="8b337-110">Uitvoer: ' A</span><span class="sxs-lookup"><span data-stu-id="8b337-110">Output : 'A</span></span>

<span data-ttu-id="8b337-111">Het eerste element van de matrix.</span><span class="sxs-lookup"><span data-stu-id="8b337-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8b337-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8b337-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="8b337-113">' A</span><span class="sxs-lookup"><span data-stu-id="8b337-113">'A</span></span>

<span data-ttu-id="8b337-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="8b337-114">The type of the array elements.</span></span>