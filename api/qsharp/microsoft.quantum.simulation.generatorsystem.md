---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Door de gebruiker gedefinieerd GeneratorSystem-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 3748d3fb79597fb526c86a91bc28290155189014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858414"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="1c0d9-102">Door de gebruiker gedefinieerd GeneratorSystem-type</span><span class="sxs-lookup"><span data-stu-id="1c0d9-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="1c0d9-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1c0d9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c0d9-105">Vertegenwoordigt een verzameling `GeneratorIndex` es.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="1c0d9-106">Deze verzameling wordt herhaald met een geheel getal met één index en er wordt aangenomen dat de grootte van de verzameling bekend is.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="1c0d9-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1c0d9-107">Remarks</span></span>

<span data-ttu-id="1c0d9-108">Instanties van `GeneratorSystem` kunnen eenvoudig worden gedefinieerd met behulp van de <xref:microsoft.quantum.arrays.lookupfunction> functie.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c0d9-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1c0d9-109">See Also</span></span>

- [<span data-ttu-id="1c0d9-110">Micro soft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="1c0d9-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)