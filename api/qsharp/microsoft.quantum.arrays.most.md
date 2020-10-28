---
uid: Microsoft.Quantum.Arrays.Most
title: De meeste functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705861"
---
# <a name="most-function"></a><span data-ttu-id="dc567-102">De meeste functie</span><span class="sxs-lookup"><span data-stu-id="dc567-102">Most function</span></span>

<span data-ttu-id="dc567-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dc567-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dc567-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc567-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc567-105">Maakt een matrix die gelijk is aan een invoer matrix, behalve dat het laatste matrix element is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="dc567-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="dc567-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dc567-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="dc567-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="dc567-107">array : 'T[]</span></span>

<span data-ttu-id="dc567-108">Een matrix waarvan de eerste naar de laatste elementen van de uitvoer matrix moet worden gevormd.</span><span class="sxs-lookup"><span data-stu-id="dc567-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="dc567-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="dc567-109">Output : 'T[]</span></span>

<span data-ttu-id="dc567-110">Een matrix met de elementen `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="dc567-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dc567-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dc567-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dc567-112">T</span><span class="sxs-lookup"><span data-stu-id="dc567-112">'T</span></span>

<span data-ttu-id="dc567-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="dc567-113">The type of the array elements.</span></span>