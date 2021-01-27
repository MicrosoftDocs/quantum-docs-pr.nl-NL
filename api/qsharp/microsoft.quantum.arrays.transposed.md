---
uid: Microsoft.Quantum.Arrays.Transposed
title: Getransponeerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850937"
---
# <a name="transposed-function"></a><span data-ttu-id="9589d-102">Getransponeerde functie</span><span class="sxs-lookup"><span data-stu-id="9589d-102">Transposed function</span></span>

<span data-ttu-id="9589d-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9589d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9589d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9589d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9589d-105">Retourneert de getransponeerde matrix die wordt weer gegeven als een matrix met matrices.</span><span class="sxs-lookup"><span data-stu-id="9589d-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="9589d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9589d-106">Description</span></span>

<span data-ttu-id="9589d-107">Invoer als $r \times c $ matrix met $r $ rows en $c $ columns.</span><span class="sxs-lookup"><span data-stu-id="9589d-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="9589d-108">De matrix is gebaseerd op rijen, dat wil zeggen, `matrix[i][j]` het element op rij $i $ en kolom $j $.</span><span class="sxs-lookup"><span data-stu-id="9589d-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="9589d-109">Deze functie retourneert de $c \times r $ matrix die de getransponeerde van de invoer matrix is.</span><span class="sxs-lookup"><span data-stu-id="9589d-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="9589d-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="9589d-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="9589d-111">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9589d-111">matrix : 'T[][]</span></span>

<span data-ttu-id="9589d-112">Op rijen gebaseerd $r \times c $ matrix</span><span class="sxs-lookup"><span data-stu-id="9589d-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="9589d-113">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9589d-113">Output : 'T[][]</span></span>

<span data-ttu-id="9589d-114">$C \times r $ matrix getransponeerd</span><span class="sxs-lookup"><span data-stu-id="9589d-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9589d-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9589d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9589d-116">T</span><span class="sxs-lookup"><span data-stu-id="9589d-116">'T</span></span>

<span data-ttu-id="9589d-117">Het type van elk element van `matrix` .</span><span class="sxs-lookup"><span data-stu-id="9589d-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="9589d-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9589d-118">Example</span></span>

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```