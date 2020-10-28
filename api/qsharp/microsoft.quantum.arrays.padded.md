---
uid: Microsoft.Quantum.Arrays.Padded
title: Functie aangevuld
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705852"
---
# <a name="padded-function"></a><span data-ttu-id="9b1dd-102">Functie aangevuld</span><span class="sxs-lookup"><span data-stu-id="9b1dd-102">Padded function</span></span>

<span data-ttu-id="9b1dd-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9b1dd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9b1dd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9b1dd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9b1dd-105">Retourneert een matrix met de opgegeven waarden tot een opgegeven lengte.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="9b1dd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9b1dd-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="9b1dd-107">nElementsTotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b1dd-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b1dd-108">De lengte van de opgevulde matrix.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-108">The length of the padded array.</span></span> <span data-ttu-id="9b1dd-109">Als dit positief is, `inputArray` wordt aan het hoofd opgevuld.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="9b1dd-110">Als dit negatief is, `inputArray` wordt aan de staart opgevuld.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="9b1dd-111">defaultElement: 'T</span><span class="sxs-lookup"><span data-stu-id="9b1dd-111">defaultElement : 'T</span></span>

<span data-ttu-id="9b1dd-112">Standaard waarde voor het gebruik van opvullings elementen.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="9b1dd-113">inputArray: 'T []</span><span class="sxs-lookup"><span data-stu-id="9b1dd-113">inputArray : 'T[]</span></span>

<span data-ttu-id="9b1dd-114">Matrix waarvan de waarden zich op het hoofd van de uitvoer matrix bevinden.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="9b1dd-115">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="9b1dd-115">Output : 'T[]</span></span>

<span data-ttu-id="9b1dd-116">Een matrix `output` die de `inputArray` opgevulde waarde bij het hoofd met `defaultElement` s tot een `output` lengte heeft `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="9b1dd-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9b1dd-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9b1dd-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9b1dd-118">T</span><span class="sxs-lookup"><span data-stu-id="9b1dd-118">'T</span></span>

<span data-ttu-id="9b1dd-119">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="9b1dd-119">The type of the array elements.</span></span>