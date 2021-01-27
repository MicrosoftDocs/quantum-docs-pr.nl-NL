---
uid: Microsoft.Quantum.Arrays.IndexRange
title: De functie IndexRange
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845785"
---
# <a name="indexrange-function"></a><span data-ttu-id="64c33-102">De functie IndexRange</span><span class="sxs-lookup"><span data-stu-id="64c33-102">IndexRange function</span></span>

<span data-ttu-id="64c33-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="64c33-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="64c33-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="64c33-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="64c33-105">Op basis van een matrix, retourneert een bereik over de indices van die matrix, die geschikt is voor gebruik in een for-lus.</span><span class="sxs-lookup"><span data-stu-id="64c33-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="64c33-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="64c33-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="64c33-107">matrix: ' TEle []</span><span class="sxs-lookup"><span data-stu-id="64c33-107">array : 'TElement[]</span></span>

<span data-ttu-id="64c33-108">Een matrix waarvoor een reeks indexen moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="64c33-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="64c33-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="64c33-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="64c33-110">Een bereik van alle indices van de matrix.</span><span class="sxs-lookup"><span data-stu-id="64c33-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="64c33-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="64c33-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="64c33-112">-TEle</span><span class="sxs-lookup"><span data-stu-id="64c33-112">'TElement</span></span>

<span data-ttu-id="64c33-113">Het type elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="64c33-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="64c33-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="64c33-114">Example</span></span>

<span data-ttu-id="64c33-115">De volgende `for` lussen zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="64c33-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```