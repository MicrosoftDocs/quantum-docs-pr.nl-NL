---
uid: Microsoft.Quantum.Arrays.Mapped
title: Toegewezen functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 00ea0803faf6e8edfa748af63dd6c7e217b1de41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845676"
---
# <a name="mapped-function"></a><span data-ttu-id="54e7c-102">Toegewezen functie</span><span class="sxs-lookup"><span data-stu-id="54e7c-102">Mapped function</span></span>

<span data-ttu-id="54e7c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="54e7c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="54e7c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="54e7c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="54e7c-105">Op basis van een matrix en een functie die is gedefinieerd voor de elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.</span><span class="sxs-lookup"><span data-stu-id="54e7c-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="54e7c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="54e7c-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="54e7c-107">Mapper: 'T-> ' U</span><span class="sxs-lookup"><span data-stu-id="54e7c-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="54e7c-108">Een functie van `'T` naar `'U` die wordt gebruikt voor het toewijzen van elementen.</span><span class="sxs-lookup"><span data-stu-id="54e7c-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="54e7c-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="54e7c-109">array : 'T[]</span></span>

<span data-ttu-id="54e7c-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="54e7c-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="54e7c-111">Uitvoer: ' U []</span><span class="sxs-lookup"><span data-stu-id="54e7c-111">Output : 'U[]</span></span>

<span data-ttu-id="54e7c-112">Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="54e7c-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="54e7c-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="54e7c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="54e7c-114">T</span><span class="sxs-lookup"><span data-stu-id="54e7c-114">'T</span></span>

<span data-ttu-id="54e7c-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="54e7c-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="54e7c-116">' U</span><span class="sxs-lookup"><span data-stu-id="54e7c-116">'U</span></span>

<span data-ttu-id="54e7c-117">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="54e7c-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e7c-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="54e7c-118">Remarks</span></span>

<span data-ttu-id="54e7c-119">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix hebben `'T[]` en een functie `mapper: 'T -> 'U` die we de elementen van de matrix kunnen toewijzen en een nieuwe matrix van het type produceren `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="54e7c-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>