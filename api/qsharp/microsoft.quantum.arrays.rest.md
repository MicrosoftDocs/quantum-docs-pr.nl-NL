---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705805"
---
# <a name="rest-function"></a><span data-ttu-id="10d29-102">Rest-functie</span><span class="sxs-lookup"><span data-stu-id="10d29-102">Rest function</span></span>

<span data-ttu-id="10d29-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="10d29-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="10d29-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10d29-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10d29-105">Maakt een matrix die gelijk is aan een invoer matrix, behalve dat het eerste matrix element wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="10d29-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="10d29-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="10d29-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="10d29-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="10d29-107">array : 'T[]</span></span>

<span data-ttu-id="10d29-108">Een matrix waarvan de seconde tot laatste elementen de uitvoer matrix vormen.</span><span class="sxs-lookup"><span data-stu-id="10d29-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="10d29-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="10d29-109">Output : 'T[]</span></span>

<span data-ttu-id="10d29-110">Een matrix met de elementen `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="10d29-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="10d29-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="10d29-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="10d29-112">T</span><span class="sxs-lookup"><span data-stu-id="10d29-112">'T</span></span>

<span data-ttu-id="10d29-113">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="10d29-113">The type of the array elements.</span></span>