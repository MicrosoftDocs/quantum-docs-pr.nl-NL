---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Functie diagonaal
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 2857046f59a958fed106af0944b75baaa3292e96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842833"
---
# <a name="diagonal-function"></a><span data-ttu-id="f8f99-102">Functie diagonaal</span><span class="sxs-lookup"><span data-stu-id="f8f99-102">Diagonal function</span></span>

<span data-ttu-id="f8f99-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f8f99-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f8f99-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f99-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f8f99-105">Hiermee wordt een matrix van diagonale elementen van een tweedimensionale matrix geretourneerd</span><span class="sxs-lookup"><span data-stu-id="f8f99-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="f8f99-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f8f99-106">Description</span></span>

<span data-ttu-id="f8f99-107">Als de tweedimensionale matrix geen vier Kante vorm heeft, wordt de diagonaal boven het minimale aantal rijen en kolommen geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f8f99-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="f8f99-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f8f99-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="f8f99-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="f8f99-109">matrix : 'T[][]</span></span>

<span data-ttu-id="f8f99-110">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="f8f99-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="f8f99-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="f8f99-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f8f99-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f8f99-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f8f99-113">T</span><span class="sxs-lookup"><span data-stu-id="f8f99-113">'T</span></span>

<span data-ttu-id="f8f99-114">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="f8f99-114">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="f8f99-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f8f99-115">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a><span data-ttu-id="f8f99-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f8f99-116">See Also</span></span>

- [<span data-ttu-id="f8f99-117">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="f8f99-117">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)