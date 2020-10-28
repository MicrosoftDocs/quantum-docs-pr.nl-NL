---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Door de gebruiker gedefinieerd GeneratorSystem-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708892"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="2d410-102">Door de gebruiker gedefinieerd GeneratorSystem-type</span><span class="sxs-lookup"><span data-stu-id="2d410-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="2d410-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2d410-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2d410-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2d410-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2d410-105">Vertegenwoordigt een verzameling `GeneratorIndex` es.</span><span class="sxs-lookup"><span data-stu-id="2d410-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="2d410-106">Deze verzameling wordt herhaald met een geheel getal met één index en er wordt aangenomen dat de grootte van de verzameling bekend is.</span><span class="sxs-lookup"><span data-stu-id="2d410-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="2d410-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2d410-107">Remarks</span></span>

<span data-ttu-id="2d410-108">Instanties van `GeneratorSystem` kunnen eenvoudig worden gedefinieerd met behulp van de <xref:microsoft.quantum.arrays.lookupfunction> functie.</span><span class="sxs-lookup"><span data-stu-id="2d410-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d410-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2d410-109">See Also</span></span>

- [<span data-ttu-id="2d410-110">Micro soft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="2d410-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)