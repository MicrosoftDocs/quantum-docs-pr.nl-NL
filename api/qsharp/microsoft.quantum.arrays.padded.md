---
uid: Microsoft.Quantum.Arrays.Padded
title: Functie aangevuld
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220532"
---
# <a name="padded-function"></a><span data-ttu-id="c12ab-102">Functie aangevuld</span><span class="sxs-lookup"><span data-stu-id="c12ab-102">Padded function</span></span>

<span data-ttu-id="c12ab-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c12ab-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c12ab-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c12ab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c12ab-105">Retourneert een matrix met de opgegeven waarden tot een opgegeven lengte.</span><span class="sxs-lookup"><span data-stu-id="c12ab-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c12ab-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c12ab-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="c12ab-107">nElementsTotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c12ab-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c12ab-108">De lengte van de opgevulde matrix.</span><span class="sxs-lookup"><span data-stu-id="c12ab-108">The length of the padded array.</span></span> <span data-ttu-id="c12ab-109">Als dit positief is, `inputArray` wordt aan het hoofd opgevuld.</span><span class="sxs-lookup"><span data-stu-id="c12ab-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="c12ab-110">Als dit negatief is, `inputArray` wordt aan de staart opgevuld.</span><span class="sxs-lookup"><span data-stu-id="c12ab-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="c12ab-111">defaultElement: 'T</span><span class="sxs-lookup"><span data-stu-id="c12ab-111">defaultElement : 'T</span></span>

<span data-ttu-id="c12ab-112">Standaard waarde voor het gebruik van opvullings elementen.</span><span class="sxs-lookup"><span data-stu-id="c12ab-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="c12ab-113">inputArray: 'T []</span><span class="sxs-lookup"><span data-stu-id="c12ab-113">inputArray : 'T[]</span></span>

<span data-ttu-id="c12ab-114">Matrix waarvan de waarden zich op het hoofd van de uitvoer matrix bevinden.</span><span class="sxs-lookup"><span data-stu-id="c12ab-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="c12ab-115">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="c12ab-115">Output : 'T[]</span></span>

<span data-ttu-id="c12ab-116">Een matrix `output` die de `inputArray` opgevulde waarde bij het hoofd met `defaultElement` s tot een `output` lengte heeft `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="c12ab-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c12ab-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c12ab-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c12ab-118">T</span><span class="sxs-lookup"><span data-stu-id="c12ab-118">'T</span></span>

<span data-ttu-id="c12ab-119">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="c12ab-119">The type of the array elements.</span></span>