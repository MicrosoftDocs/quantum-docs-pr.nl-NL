---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845545"
---
# <a name="partitioned-function"></a><span data-ttu-id="ddee5-102">Gepartitioneerde functie</span><span class="sxs-lookup"><span data-stu-id="ddee5-102">Partitioned function</span></span>

<span data-ttu-id="ddee5-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ddee5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ddee5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ddee5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ddee5-105">Hiermee splitst u een matrix in meerdere delen.</span><span class="sxs-lookup"><span data-stu-id="ddee5-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="ddee5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ddee5-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="ddee5-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ddee5-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ddee5-108">Aantal elementen in elk deel van de matrix</span><span class="sxs-lookup"><span data-stu-id="ddee5-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="ddee5-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="ddee5-109">arr : 'T[]</span></span>

<span data-ttu-id="ddee5-110">De invoer matrix die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="ddee5-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="ddee5-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="ddee5-111">Output : 'T[][]</span></span>

<span data-ttu-id="ddee5-112">Meerdere matrices waarbij de eerste matrix het eerste is `nElements[0]` `arr` en de tweede matrix, `nElements[1]` `arr` enzovoort. De laatste matrix bevat alle resterende elementen.</span><span class="sxs-lookup"><span data-stu-id="ddee5-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ddee5-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ddee5-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ddee5-114">T</span><span class="sxs-lookup"><span data-stu-id="ddee5-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="ddee5-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ddee5-115">Example</span></span>

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```