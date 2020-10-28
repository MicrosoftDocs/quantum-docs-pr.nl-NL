---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: De functie ColumnAt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706165"
---
# <a name="columnat-function"></a><span data-ttu-id="9e088-102">De functie ColumnAt</span><span class="sxs-lookup"><span data-stu-id="9e088-102">ColumnAt function</span></span>

<span data-ttu-id="9e088-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9e088-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9e088-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e088-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e088-105">Hiermee wordt een kolom uit een matrix opgehaald.</span><span class="sxs-lookup"><span data-stu-id="9e088-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="9e088-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9e088-106">Description</span></span>

<span data-ttu-id="9e088-107">Met deze functie wordt een kolom in een matrix geëxtraheerd in de volg orde van rijen.</span><span class="sxs-lookup"><span data-stu-id="9e088-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="9e088-108">Het extra heren van een rij-corrsponds om toegang te krijgen tot elementen van de eerste index. hiervoor is daarom geen verdere behandeling vereist.</span><span class="sxs-lookup"><span data-stu-id="9e088-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="9e088-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e088-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="9e088-110">kolom: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e088-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e088-111">Kolom van de matrix</span><span class="sxs-lookup"><span data-stu-id="9e088-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="9e088-112">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9e088-112">matrix : 'T[][]</span></span>

<span data-ttu-id="9e088-113">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="9e088-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="9e088-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="9e088-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9e088-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9e088-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e088-116">T</span><span class="sxs-lookup"><span data-stu-id="9e088-116">'T</span></span>

<span data-ttu-id="9e088-117">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="9e088-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e088-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9e088-118">See Also</span></span>

- [<span data-ttu-id="9e088-119">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="9e088-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="9e088-120">Micro soft. Quantum. arrays. diagonaal</span><span class="sxs-lookup"><span data-stu-id="9e088-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)