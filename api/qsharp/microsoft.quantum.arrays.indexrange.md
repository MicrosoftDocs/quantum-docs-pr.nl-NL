---
uid: Microsoft.Quantum.Arrays.IndexRange
title: De functie IndexRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220940"
---
# <a name="indexrange-function"></a><span data-ttu-id="3ff15-102">De functie IndexRange</span><span class="sxs-lookup"><span data-stu-id="3ff15-102">IndexRange function</span></span>

<span data-ttu-id="3ff15-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3ff15-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3ff15-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ff15-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ff15-105">Op basis van een matrix, retourneert een bereik over de indices van die matrix, die geschikt is voor gebruik in een for-lus.</span><span class="sxs-lookup"><span data-stu-id="3ff15-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="3ff15-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ff15-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="3ff15-107">matrix: ' TEle []</span><span class="sxs-lookup"><span data-stu-id="3ff15-107">array : 'TElement[]</span></span>

<span data-ttu-id="3ff15-108">Een matrix waarvoor een reeks indexen moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3ff15-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="3ff15-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="3ff15-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="3ff15-110">Een bereik van alle indices van de matrix.</span><span class="sxs-lookup"><span data-stu-id="3ff15-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3ff15-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3ff15-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="3ff15-112">-TEle</span><span class="sxs-lookup"><span data-stu-id="3ff15-112">'TElement</span></span>

<span data-ttu-id="3ff15-113">Het type elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="3ff15-113">The type of elements of the array.</span></span>