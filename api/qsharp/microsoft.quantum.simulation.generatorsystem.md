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
# <a name="generatorsystem-user-defined-type"></a>Door de gebruiker gedefinieerd GeneratorSystem-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een verzameling `GeneratorIndex` es.

Deze verzameling wordt herhaald met een geheel getal met één index en er wordt aangenomen dat de grootte van de verzameling bekend is.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Opmerkingen

Instanties van `GeneratorSystem` kunnen eenvoudig worden gedefinieerd met behulp van de <xref:microsoft.quantum.arrays.lookupfunction> functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. LookupFunction](xref:Microsoft.Quantum.Arrays.LookupFunction)