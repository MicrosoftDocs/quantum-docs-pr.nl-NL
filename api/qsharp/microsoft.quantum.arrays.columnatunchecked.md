---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: De functie ColumnAtUnchecked
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 06fce23bbf7142ee0e0b0ed3f2c0578676f2097b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221586"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="c3e21-102">De functie ColumnAtUnchecked</span><span class="sxs-lookup"><span data-stu-id="c3e21-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="c3e21-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c3e21-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c3e21-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c3e21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c3e21-105">Deze functie controleert niet op matrix vorm</span><span class="sxs-lookup"><span data-stu-id="c3e21-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="c3e21-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c3e21-106">Description</span></span>

<span data-ttu-id="c3e21-107">Deze functie kan worden gebruikt in andere multidimensionale functies, waarbij de invoer matrix al wordt gecontroleerd op een geldige rechthoekige vorm.</span><span class="sxs-lookup"><span data-stu-id="c3e21-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="c3e21-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c3e21-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="c3e21-109">kolom: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3e21-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="c3e21-110">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="c3e21-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="c3e21-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="c3e21-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c3e21-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c3e21-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c3e21-113">T</span><span class="sxs-lookup"><span data-stu-id="c3e21-113">'T</span></span>

