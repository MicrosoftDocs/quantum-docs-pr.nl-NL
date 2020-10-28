---
uid: Microsoft.Quantum.Arrays.Prefixes
title: De functie voor voegsels
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705821"
---
# <a name="prefixes-function"></a><span data-ttu-id="17b12-102">De functie voor voegsels</span><span class="sxs-lookup"><span data-stu-id="17b12-102">Prefixes function</span></span>

<span data-ttu-id="17b12-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="17b12-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="17b12-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17b12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17b12-105">Op basis van een matrix, worden alle bijbehorende voor voegsels geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="17b12-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="17b12-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="17b12-106">Description</span></span>

<span data-ttu-id="17b12-107">Retourneert een matrix van alle voor voegsels, beginnend met een matrix die alleen het eerste element tot de volledige matrix heeft.</span><span class="sxs-lookup"><span data-stu-id="17b12-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="17b12-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="17b12-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="17b12-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="17b12-109">array : 'T[]</span></span>

<span data-ttu-id="17b12-110">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="17b12-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="17b12-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="17b12-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="17b12-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="17b12-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="17b12-113">T</span><span class="sxs-lookup"><span data-stu-id="17b12-113">'T</span></span>

<span data-ttu-id="17b12-114">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="17b12-114">The type of `array` elements.</span></span>