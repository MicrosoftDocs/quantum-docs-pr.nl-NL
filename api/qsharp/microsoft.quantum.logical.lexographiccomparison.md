---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: De functie LexographicComparison
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: f0b68974a0ea26907b58971e4fa4b1f06f5714d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701439"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="9dde6-102">De functie LexographicComparison</span><span class="sxs-lookup"><span data-stu-id="9dde6-102">LexographicComparison function</span></span>

<span data-ttu-id="9dde6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9dde6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9dde6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9dde6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9dde6-105">Op basis van een vergelijkings functie retourneert een nieuwe functie die lexographically twee matrices vergelijkt.</span><span class="sxs-lookup"><span data-stu-id="9dde6-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="9dde6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9dde6-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="9dde6-107">elementComparison: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9dde6-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9dde6-108">Een functie die twee elementen vergelijkt `x` en `y` retourneert als deze `x` kleiner is dan of gelijk is aan `y` .</span><span class="sxs-lookup"><span data-stu-id="9dde6-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="9dde6-109">Output: ('T [], 'T [])-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9dde6-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9dde6-110">Een functie die twee matrices vergelijkt `xs` en `ys` retourneert als deze `xs` voor of gelijk is aan `ys` in lexographical-volg orde.</span><span class="sxs-lookup"><span data-stu-id="9dde6-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9dde6-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9dde6-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9dde6-112">T</span><span class="sxs-lookup"><span data-stu-id="9dde6-112">'T</span></span>

<span data-ttu-id="9dde6-113">Het type van de elementen van de matrices die worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9dde6-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dde6-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9dde6-114">Remarks</span></span>

<span data-ttu-id="9dde6-115">De lexographic vergelijking tussen twee matrices `xs` en `ys` wordt gedefinieerd door de volgende procedure.</span><span class="sxs-lookup"><span data-stu-id="9dde6-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="9dde6-116">We zeggen dat twee elementen `x` en `y` gelijkwaardig zijn als `elementComparison(x, y)` en `elementComparison(y, x)` beide waar zijn.</span><span class="sxs-lookup"><span data-stu-id="9dde6-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="9dde6-117">Beide matrices worden tot het eerste paar elementen vergeleken die niet gelijk zijn aan het element.</span><span class="sxs-lookup"><span data-stu-id="9dde6-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="9dde6-118">De matrix met het element dat als eerste plaatsvindt volgens de naam die `elementComparison` als eerste moet worden uitgevoerd in de lexographical-volg orde.</span><span class="sxs-lookup"><span data-stu-id="9dde6-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="9dde6-119">Als er geen equivalente elementen worden gevonden en één matrix langer is dan de andere, wordt de kortere matrix als eerste gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9dde6-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dde6-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9dde6-120">See Also</span></span>

- [<span data-ttu-id="9dde6-121">Micro soft. Quantum. arrays. gesorteerd</span><span class="sxs-lookup"><span data-stu-id="9dde6-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)