---
uid: Microsoft.Quantum.Arrays.IndexOf
title: De functie IndexOf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848512"
---
# <a name="indexof-function"></a><span data-ttu-id="361f8-102">De functie IndexOf</span><span class="sxs-lookup"><span data-stu-id="361f8-102">IndexOf function</span></span>

<span data-ttu-id="361f8-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="361f8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="361f8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="361f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="361f8-105">Retourneert de eerste index van het eerste element in een matrix die voldoet aan een bepaald predicaat.</span><span class="sxs-lookup"><span data-stu-id="361f8-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="361f8-106">Als dit element niet bestaat, retourneert-1.</span><span class="sxs-lookup"><span data-stu-id="361f8-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="361f8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="361f8-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="361f8-108">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="361f8-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="361f8-109">Een predikaatshape die wordt gebruikt voor elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="361f8-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="361f8-110">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="361f8-110">arr : 'T[]</span></span>

<span data-ttu-id="361f8-111">Een matrix die moet worden doorzocht met behulp van het opgegeven predicaat.</span><span class="sxs-lookup"><span data-stu-id="361f8-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="361f8-112">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="361f8-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="361f8-113">De kleinste index `idx` `predicate(arr[idx])` , bijvoorbeeld waar, of-1 als er geen dergelijk element bestaat.</span><span class="sxs-lookup"><span data-stu-id="361f8-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="361f8-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="361f8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="361f8-115">T</span><span class="sxs-lookup"><span data-stu-id="361f8-115">'T</span></span>



## <a name="example"></a><span data-ttu-id="361f8-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="361f8-116">Example</span></span>

<span data-ttu-id="361f8-117">Stel dat dit `IsEven : Int -> Bool` een functie is die als resultaat wordt gegeven `true` als de invoer van een even getal is.</span><span class="sxs-lookup"><span data-stu-id="361f8-117">Suppose that `IsEven : Int -> Bool` is a function that returns `true` if and only if its input is even.</span></span> <span data-ttu-id="361f8-118">Dit kan vervolgens worden gebruikt `IndexOf` om het eerste even element in een matrix te vinden:</span><span class="sxs-lookup"><span data-stu-id="361f8-118">Then, this can be used with `IndexOf` to find the first even element in an array:</span></span>

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```