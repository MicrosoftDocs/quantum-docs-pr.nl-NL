---
uid: Microsoft.Quantum.Arrays.Flattened
title: Platte functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 91a35f0ac2c2f8609bac07734265fcf4e88bf50b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706021"
---
# <a name="flattened-function"></a><span data-ttu-id="a5509-102">Platte functie</span><span class="sxs-lookup"><span data-stu-id="a5509-102">Flattened function</span></span>

<span data-ttu-id="a5509-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a5509-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a5509-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a5509-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a5509-105">Met een matrix van matrices wordt de samen voeging van alle matrices geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="a5509-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a5509-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a5509-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="a5509-107">matrices: ' [] []</span><span class="sxs-lookup"><span data-stu-id="a5509-107">arrays : 'T[][]</span></span>

<span data-ttu-id="a5509-108">Matrix van matrices.</span><span class="sxs-lookup"><span data-stu-id="a5509-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="a5509-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="a5509-109">Output : 'T[]</span></span>

<span data-ttu-id="a5509-110">Samen voeging van alle matrices.</span><span class="sxs-lookup"><span data-stu-id="a5509-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a5509-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a5509-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a5509-112">T</span><span class="sxs-lookup"><span data-stu-id="a5509-112">'T</span></span>

<span data-ttu-id="a5509-113">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="a5509-113">The type of `array` elements.</span></span>