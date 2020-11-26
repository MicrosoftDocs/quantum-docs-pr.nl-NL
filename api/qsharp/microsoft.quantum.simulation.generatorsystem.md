---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Door de gebruiker gedefinieerd GeneratorSystem-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 20092a8deca50c90f46f4d79c6b40b805f135754
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225224"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="3e574-102">Door de gebruiker gedefinieerd GeneratorSystem-type</span><span class="sxs-lookup"><span data-stu-id="3e574-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="3e574-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="3e574-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="3e574-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e574-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e574-105">Vertegenwoordigt een verzameling `GeneratorIndex` es.</span><span class="sxs-lookup"><span data-stu-id="3e574-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="3e574-106">Deze verzameling wordt herhaald met een geheel getal met één index en er wordt aangenomen dat de grootte van de verzameling bekend is.</span><span class="sxs-lookup"><span data-stu-id="3e574-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="3e574-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3e574-107">Remarks</span></span>

<span data-ttu-id="3e574-108">Instanties van `GeneratorSystem` kunnen eenvoudig worden gedefinieerd met behulp van de <xref:microsoft.quantum.arrays.lookupfunction> functie.</span><span class="sxs-lookup"><span data-stu-id="3e574-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e574-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3e574-109">See Also</span></span>

- [<span data-ttu-id="3e574-110">Micro soft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="3e574-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)