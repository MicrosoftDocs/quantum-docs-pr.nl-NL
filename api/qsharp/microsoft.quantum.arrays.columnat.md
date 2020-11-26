---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: De functie ColumnAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210095"
---
# <a name="columnat-function"></a><span data-ttu-id="14caa-102">De functie ColumnAt</span><span class="sxs-lookup"><span data-stu-id="14caa-102">ColumnAt function</span></span>

<span data-ttu-id="14caa-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="14caa-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="14caa-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14caa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14caa-105">Hiermee wordt een kolom uit een matrix opgehaald.</span><span class="sxs-lookup"><span data-stu-id="14caa-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="14caa-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="14caa-106">Description</span></span>

<span data-ttu-id="14caa-107">Met deze functie wordt een kolom in een matrix geëxtraheerd in de volg orde van rijen.</span><span class="sxs-lookup"><span data-stu-id="14caa-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="14caa-108">Het extra heren van een rij-corrsponds om toegang te krijgen tot elementen van de eerste index. hiervoor is daarom geen verdere behandeling vereist.</span><span class="sxs-lookup"><span data-stu-id="14caa-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="14caa-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="14caa-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="14caa-110">kolom: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14caa-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14caa-111">Kolom van de matrix</span><span class="sxs-lookup"><span data-stu-id="14caa-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="14caa-112">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="14caa-112">matrix : 'T[][]</span></span>

<span data-ttu-id="14caa-113">2-dimensionale matrix in de volg orde van rijen</span><span class="sxs-lookup"><span data-stu-id="14caa-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="14caa-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="14caa-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="14caa-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="14caa-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14caa-116">T</span><span class="sxs-lookup"><span data-stu-id="14caa-116">'T</span></span>

<span data-ttu-id="14caa-117">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="14caa-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="14caa-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="14caa-118">See Also</span></span>

- [<span data-ttu-id="14caa-119">Micro soft. Quantum. arrays. getransponeerde</span><span class="sxs-lookup"><span data-stu-id="14caa-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="14caa-120">Micro soft. Quantum. arrays. diagonaal</span><span class="sxs-lookup"><span data-stu-id="14caa-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)