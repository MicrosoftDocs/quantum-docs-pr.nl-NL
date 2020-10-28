---
uid: Microsoft.Quantum.Arrays.Reversed
title: Omgekeerde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705804"
---
# <a name="reversed-function"></a><span data-ttu-id="97d27-102">Omgekeerde functie</span><span class="sxs-lookup"><span data-stu-id="97d27-102">Reversed function</span></span>

<span data-ttu-id="97d27-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="97d27-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="97d27-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="97d27-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="97d27-105">Maak een matrix die dezelfde elementen bevat als een invoer matrix, maar in omgekeerde volg orde.</span><span class="sxs-lookup"><span data-stu-id="97d27-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="97d27-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="97d27-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="97d27-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="97d27-107">array : 'T[]</span></span>

<span data-ttu-id="97d27-108">Een matrix waarvan de elementen in omgekeerde volg orde moeten worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="97d27-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="97d27-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="97d27-109">Output : 'T[]</span></span>

<span data-ttu-id="97d27-110">Een matrix met de elementen `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="97d27-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="97d27-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="97d27-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="97d27-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="97d27-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97d27-113">T</span><span class="sxs-lookup"><span data-stu-id="97d27-113">'T</span></span>

<span data-ttu-id="97d27-114">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="97d27-114">The type of the array elements.</span></span>