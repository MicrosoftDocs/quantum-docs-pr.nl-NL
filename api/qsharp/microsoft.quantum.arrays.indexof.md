---
uid: Microsoft.Quantum.Arrays.IndexOf
title: De functie IndexOf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705980"
---
# <a name="indexof-function"></a><span data-ttu-id="b20e0-102">De functie IndexOf</span><span class="sxs-lookup"><span data-stu-id="b20e0-102">IndexOf function</span></span>

<span data-ttu-id="b20e0-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b20e0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b20e0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b20e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b20e0-105">Retourneert de eerste index van het eerste element in een matrix die voldoet aan een bepaald predicaat.</span><span class="sxs-lookup"><span data-stu-id="b20e0-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="b20e0-106">Als dit element niet bestaat, retourneert-1.</span><span class="sxs-lookup"><span data-stu-id="b20e0-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="b20e0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="b20e0-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="b20e0-108">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b20e0-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b20e0-109">Een predikaatshape die wordt gebruikt voor elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="b20e0-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="b20e0-110">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="b20e0-110">arr : 'T[]</span></span>

<span data-ttu-id="b20e0-111">Een matrix die moet worden doorzocht met behulp van het opgegeven predicaat.</span><span class="sxs-lookup"><span data-stu-id="b20e0-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="b20e0-112">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b20e0-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b20e0-113">De kleinste index `idx` `predicate(arr[idx])` , bijvoorbeeld waar, of-1 als er geen dergelijk element bestaat.</span><span class="sxs-lookup"><span data-stu-id="b20e0-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b20e0-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b20e0-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b20e0-115">T</span><span class="sxs-lookup"><span data-stu-id="b20e0-115">'T</span></span>

