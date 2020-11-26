---
uid: Microsoft.Quantum.Arrays.Reversed
title: Omgekeerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220430"
---
# <a name="reversed-function"></a><span data-ttu-id="9eef1-102">Omgekeerde functie</span><span class="sxs-lookup"><span data-stu-id="9eef1-102">Reversed function</span></span>

<span data-ttu-id="9eef1-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9eef1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9eef1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9eef1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9eef1-105">Maak een matrix die dezelfde elementen bevat als een invoer matrix, maar in omgekeerde volg orde.</span><span class="sxs-lookup"><span data-stu-id="9eef1-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="9eef1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9eef1-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="9eef1-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="9eef1-107">array : 'T[]</span></span>

<span data-ttu-id="9eef1-108">Een matrix waarvan de elementen in omgekeerde volg orde moeten worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="9eef1-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="9eef1-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="9eef1-109">Output : 'T[]</span></span>

<span data-ttu-id="9eef1-110">Een matrix met de elementen `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="9eef1-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="9eef1-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="9eef1-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9eef1-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9eef1-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9eef1-113">T</span><span class="sxs-lookup"><span data-stu-id="9eef1-113">'T</span></span>

<span data-ttu-id="9eef1-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="9eef1-114">The type of the array elements.</span></span>