---
uid: Microsoft.Quantum.Arrays.Transposed
title: Getransponeerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219988"
---
# <a name="transposed-function"></a><span data-ttu-id="9d3c0-102">Getransponeerde functie</span><span class="sxs-lookup"><span data-stu-id="9d3c0-102">Transposed function</span></span>

<span data-ttu-id="9d3c0-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9d3c0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9d3c0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d3c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d3c0-105">Retourneert de getransponeerde matrix die wordt weer gegeven als een matrix met matrices.</span><span class="sxs-lookup"><span data-stu-id="9d3c0-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="9d3c0-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9d3c0-106">Description</span></span>

<span data-ttu-id="9d3c0-107">Invoer als $r \times c $ matrix met $r $ rows en $c $ columns.</span><span class="sxs-lookup"><span data-stu-id="9d3c0-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="9d3c0-108">De matrix is gebaseerd op rijen, dat wil zeggen, `matrix[i][j]` het element op rij $i $ en kolom $j $.</span><span class="sxs-lookup"><span data-stu-id="9d3c0-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="9d3c0-109">Deze functie retourneert de $c \times r $ matrix die de getransponeerde van de invoer matrix is.</span><span class="sxs-lookup"><span data-stu-id="9d3c0-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="9d3c0-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="9d3c0-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="9d3c0-111">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9d3c0-111">matrix : 'T[][]</span></span>

<span data-ttu-id="9d3c0-112">Op rijen gebaseerd $r \times c $ matrix</span><span class="sxs-lookup"><span data-stu-id="9d3c0-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="9d3c0-113">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9d3c0-113">Output : 'T[][]</span></span>

<span data-ttu-id="9d3c0-114">$C \times r $ matrix getransponeerd</span><span class="sxs-lookup"><span data-stu-id="9d3c0-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9d3c0-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9d3c0-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d3c0-116">T</span><span class="sxs-lookup"><span data-stu-id="9d3c0-116">'T</span></span>

<span data-ttu-id="9d3c0-117">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="9d3c0-117">The type of each element of `matrix`.</span></span>