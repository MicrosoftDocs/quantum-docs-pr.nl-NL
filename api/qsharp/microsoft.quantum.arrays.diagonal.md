---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Functie diagonaal
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 180b7185c94d712fa02100cb97abfbb6c464d12a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706117"
---
# <a name="diagonal-function"></a><span data-ttu-id="972a9-102">Functie diagonaal</span><span class="sxs-lookup"><span data-stu-id="972a9-102">Diagonal function</span></span>

<span data-ttu-id="972a9-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="972a9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="972a9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="972a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="972a9-105">Hiermee wordt een matrix van diagonale elementen van een tweedimensionale matrix geretourneerd</span><span class="sxs-lookup"><span data-stu-id="972a9-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="972a9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="972a9-106">Description</span></span>

<span data-ttu-id="972a9-107">Als de tweedimensionale matrix geen vier Kante vorm heeft, wordt de diagonaal boven het minimale aantal rijen en kolommen geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="972a9-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="972a9-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="972a9-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="972a9-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="972a9-109">matrix : 'T[][]</span></span>

<span data-ttu-id="972a9-110">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="972a9-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="972a9-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="972a9-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="972a9-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="972a9-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="972a9-113">T</span><span class="sxs-lookup"><span data-stu-id="972a9-113">'T</span></span>

<span data-ttu-id="972a9-114">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="972a9-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="972a9-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="972a9-115">See Also</span></span>

- [<span data-ttu-id="972a9-116">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="972a9-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)