---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: De functie ColumnAtUnchecked
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706164"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="d5683-102">De functie ColumnAtUnchecked</span><span class="sxs-lookup"><span data-stu-id="d5683-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="d5683-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d5683-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d5683-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5683-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5683-105">Deze functie controleert niet op matrix vorm</span><span class="sxs-lookup"><span data-stu-id="d5683-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="d5683-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d5683-106">Description</span></span>

<span data-ttu-id="d5683-107">Deze functie kan worden gebruikt in andere multidimensionale functies, waarbij de invoer matrix al wordt gecontroleerd op een geldige rechthoekige vorm.</span><span class="sxs-lookup"><span data-stu-id="d5683-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="d5683-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d5683-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="d5683-109">kolom: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d5683-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="d5683-110">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="d5683-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="d5683-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="d5683-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d5683-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d5683-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5683-113">T</span><span class="sxs-lookup"><span data-stu-id="d5683-113">'T</span></span>

