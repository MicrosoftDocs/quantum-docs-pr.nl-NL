---
uid: Microsoft.Quantum.Arrays.Count
title: Functie Count
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: e178ee63526e3485e8cc83a3ba8f827d8ecac552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842836"
---
# <a name="count-function"></a><span data-ttu-id="71632-102">Functie Count</span><span class="sxs-lookup"><span data-stu-id="71632-102">Count function</span></span>

<span data-ttu-id="71632-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="71632-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="71632-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71632-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71632-105">Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, retourneert het aantal elementen een matrix die bestaat uit die elementen die voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="71632-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="71632-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="71632-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="71632-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="71632-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="71632-108">Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.</span><span class="sxs-lookup"><span data-stu-id="71632-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="71632-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="71632-109">array : 'T[]</span></span>

<span data-ttu-id="71632-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="71632-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="71632-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="71632-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="71632-112">Het aantal elementen in `array` dat voldoet aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="71632-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="71632-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="71632-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71632-114">T</span><span class="sxs-lookup"><span data-stu-id="71632-114">'T</span></span>

<span data-ttu-id="71632-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="71632-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="71632-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="71632-116">Example</span></span>

<span data-ttu-id="71632-117">De volgende code toont de functie aantal.</span><span class="sxs-lookup"><span data-stu-id="71632-117">The following code demonstrates the "Count" function.</span></span>
<span data-ttu-id="71632-118">Een predikaat is gedefinieerd met behulp van de @"microsoft.quantum.logical.greaterthani" functie:</span><span class="sxs-lookup"><span data-stu-id="71632-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
 let predicate = GreaterThanI(_, 5);
 let count = Count(predicate, [2, 5, 9, 1, 8]);
 // count = 2
```

## <a name="remarks"></a><span data-ttu-id="71632-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="71632-119">Remarks</span></span>

<span data-ttu-id="71632-120">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een predikaat hebben waarop `'T -> Bool` we elementen kunnen filteren.</span><span class="sxs-lookup"><span data-stu-id="71632-120">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>