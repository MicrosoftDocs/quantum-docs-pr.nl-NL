---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Functie diagonaal
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221535"
---
# <a name="diagonal-function"></a><span data-ttu-id="6c090-102">Functie diagonaal</span><span class="sxs-lookup"><span data-stu-id="6c090-102">Diagonal function</span></span>

<span data-ttu-id="6c090-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6c090-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6c090-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6c090-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6c090-105">Hiermee wordt een matrix van diagonale elementen van een tweedimensionale matrix geretourneerd</span><span class="sxs-lookup"><span data-stu-id="6c090-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="6c090-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6c090-106">Description</span></span>

<span data-ttu-id="6c090-107">Als de tweedimensionale matrix geen vier Kante vorm heeft, wordt de diagonaal boven het minimale aantal rijen en kolommen geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="6c090-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="6c090-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6c090-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="6c090-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="6c090-109">matrix : 'T[][]</span></span>

<span data-ttu-id="6c090-110">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="6c090-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="6c090-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="6c090-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6c090-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6c090-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6c090-113">T</span><span class="sxs-lookup"><span data-stu-id="6c090-113">'T</span></span>

<span data-ttu-id="6c090-114">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="6c090-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c090-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6c090-115">See Also</span></span>

- [<span data-ttu-id="6c090-116">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="6c090-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)