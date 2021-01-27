---
uid: Microsoft.Quantum.Arrays.Prefixes
title: De functie voor voegsels
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845517"
---
# <a name="prefixes-function"></a><span data-ttu-id="2e6ad-102">De functie voor voegsels</span><span class="sxs-lookup"><span data-stu-id="2e6ad-102">Prefixes function</span></span>

<span data-ttu-id="2e6ad-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e6ad-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e6ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e6ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e6ad-105">Op basis van een matrix, worden alle bijbehorende voor voegsels geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="2e6ad-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2e6ad-106">Description</span></span>

<span data-ttu-id="2e6ad-107">Retourneert een matrix van alle voor voegsels, beginnend met een matrix die alleen het eerste element tot de volledige matrix heeft.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="2e6ad-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="2e6ad-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="2e6ad-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="2e6ad-109">array : 'T[]</span></span>

<span data-ttu-id="2e6ad-110">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="2e6ad-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="2e6ad-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2e6ad-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2e6ad-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e6ad-113">T</span><span class="sxs-lookup"><span data-stu-id="2e6ad-113">'T</span></span>

<span data-ttu-id="2e6ad-114">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-114">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="2e6ad-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2e6ad-115">Example</span></span>

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```