---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: De functie ColumnAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846259"
---
# <a name="columnat-function"></a><span data-ttu-id="6b971-102">De functie ColumnAt</span><span class="sxs-lookup"><span data-stu-id="6b971-102">ColumnAt function</span></span>

<span data-ttu-id="6b971-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6b971-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6b971-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b971-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b971-105">Hiermee wordt een kolom uit een matrix opgehaald.</span><span class="sxs-lookup"><span data-stu-id="6b971-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="6b971-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6b971-106">Description</span></span>

<span data-ttu-id="6b971-107">Met deze functie wordt een kolom in een matrix geëxtraheerd in de volg orde van rijen.</span><span class="sxs-lookup"><span data-stu-id="6b971-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="6b971-108">Het extra heren van een rij-corrsponds om toegang te krijgen tot elementen van de eerste index. hiervoor is daarom geen verdere behandeling vereist.</span><span class="sxs-lookup"><span data-stu-id="6b971-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="6b971-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="6b971-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="6b971-110">kolom: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b971-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6b971-111">Kolom van de matrix</span><span class="sxs-lookup"><span data-stu-id="6b971-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="6b971-112">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="6b971-112">matrix : 'T[][]</span></span>

<span data-ttu-id="6b971-113">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="6b971-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="6b971-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="6b971-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6b971-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6b971-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6b971-116">T</span><span class="sxs-lookup"><span data-stu-id="6b971-116">'T</span></span>

<span data-ttu-id="6b971-117">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="6b971-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="6b971-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6b971-118">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a><span data-ttu-id="6b971-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6b971-119">See Also</span></span>

- [<span data-ttu-id="6b971-120">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="6b971-120">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="6b971-121">Micro soft. Quantum. arrays. diagonaal</span><span class="sxs-lookup"><span data-stu-id="6b971-121">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)