---
uid: Microsoft.Quantum.Arrays.Prefixes
title: De functie voor voegsels
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220382"
---
# <a name="prefixes-function"></a><span data-ttu-id="47f3e-102">De functie voor voegsels</span><span class="sxs-lookup"><span data-stu-id="47f3e-102">Prefixes function</span></span>

<span data-ttu-id="47f3e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="47f3e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="47f3e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47f3e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47f3e-105">Op basis van een matrix, worden alle bijbehorende voor voegsels geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="47f3e-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="47f3e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="47f3e-106">Description</span></span>

<span data-ttu-id="47f3e-107">Retourneert een matrix van alle voor voegsels, beginnend met een matrix die alleen het eerste element tot de volledige matrix heeft.</span><span class="sxs-lookup"><span data-stu-id="47f3e-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="47f3e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="47f3e-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="47f3e-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="47f3e-109">array : 'T[]</span></span>

<span data-ttu-id="47f3e-110">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="47f3e-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="47f3e-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="47f3e-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47f3e-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="47f3e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47f3e-113">T</span><span class="sxs-lookup"><span data-stu-id="47f3e-113">'T</span></span>

<span data-ttu-id="47f3e-114">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="47f3e-114">The type of `array` elements.</span></span>