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
# <a name="generatorsystem-user-defined-type"></a>Door de gebruiker gedefinieerd GeneratorSystem-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een verzameling `GeneratorIndex` es.

Deze verzameling wordt herhaald met een geheel getal met één index en er wordt aangenomen dat de grootte van de verzameling bekend is.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Opmerkingen

Instanties van `GeneratorSystem` kunnen eenvoudig worden gedefinieerd met behulp van de <xref:microsoft.quantum.arrays.lookupfunction> functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. LookupFunction](xref:Microsoft.Quantum.Arrays.LookupFunction)