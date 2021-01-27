---
uid: Microsoft.Quantum.Arrays.Reversed
title: Omgekeerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845463"
---
# <a name="reversed-function"></a><span data-ttu-id="b940f-102">Omgekeerde functie</span><span class="sxs-lookup"><span data-stu-id="b940f-102">Reversed function</span></span>

<span data-ttu-id="b940f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b940f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b940f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b940f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b940f-105">Maak een matrix die dezelfde elementen bevat als een invoer matrix, maar in omgekeerde volg orde.</span><span class="sxs-lookup"><span data-stu-id="b940f-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b940f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b940f-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="b940f-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="b940f-107">array : 'T[]</span></span>

<span data-ttu-id="b940f-108">Een matrix waarvan de elementen in omgekeerde volg orde moeten worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b940f-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="b940f-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="b940f-109">Output : 'T[]</span></span>

<span data-ttu-id="b940f-110">Een matrix met de elementen `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="b940f-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="b940f-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="b940f-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b940f-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b940f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b940f-113">T</span><span class="sxs-lookup"><span data-stu-id="b940f-113">'T</span></span>

<span data-ttu-id="b940f-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="b940f-114">The type of the array elements.</span></span>