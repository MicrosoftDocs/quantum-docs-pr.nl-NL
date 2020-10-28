---
uid: Microsoft.Quantum.Arrays.IndexRange
title: De functie IndexRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705964"
---
# <a name="indexrange-function"></a><span data-ttu-id="cb0cd-102">De functie IndexRange</span><span class="sxs-lookup"><span data-stu-id="cb0cd-102">IndexRange function</span></span>

<span data-ttu-id="cb0cd-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cb0cd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cb0cd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cb0cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cb0cd-105">Op basis van een matrix, retourneert een bereik over de indices van die matrix, die geschikt is voor gebruik in een for-lus.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="cb0cd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cb0cd-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="cb0cd-107">matrix: ' TEle []</span><span class="sxs-lookup"><span data-stu-id="cb0cd-107">array : 'TElement[]</span></span>

<span data-ttu-id="cb0cd-108">Een matrix waarvoor een reeks indexen moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="cb0cd-109">Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="cb0cd-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="cb0cd-110">Een bereik van alle indices van de matrix.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cb0cd-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cb0cd-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="cb0cd-112">-TEle</span><span class="sxs-lookup"><span data-stu-id="cb0cd-112">'TElement</span></span>

<span data-ttu-id="cb0cd-113">Het type elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-113">The type of elements of the array.</span></span>