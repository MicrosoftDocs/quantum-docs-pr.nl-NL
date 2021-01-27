---
uid: Microsoft.Quantum.Arrays.Most
title: De meeste functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845584"
---
# <a name="most-function"></a><span data-ttu-id="74238-102">De meeste functie</span><span class="sxs-lookup"><span data-stu-id="74238-102">Most function</span></span>

<span data-ttu-id="74238-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="74238-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="74238-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74238-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74238-105">Maakt een matrix die gelijk is aan een invoer matrix, behalve dat het laatste matrix element is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="74238-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="74238-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="74238-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="74238-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="74238-107">array : 'T[]</span></span>

<span data-ttu-id="74238-108">Een matrix waarvan de eerste naar de laatste elementen van de uitvoer matrix moet worden gevormd.</span><span class="sxs-lookup"><span data-stu-id="74238-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="74238-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="74238-109">Output : 'T[]</span></span>

<span data-ttu-id="74238-110">Een matrix met de elementen `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="74238-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="74238-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="74238-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="74238-112">T</span><span class="sxs-lookup"><span data-stu-id="74238-112">'T</span></span>

<span data-ttu-id="74238-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="74238-113">The type of the array elements.</span></span>