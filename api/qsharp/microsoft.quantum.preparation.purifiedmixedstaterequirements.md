---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: De functie PurifiedMixedStateRequirements
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229984"
---
# <a name="purifiedmixedstaterequirements-function"></a>De functie PurifiedMixedStateRequirements

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert het totale aantal qubits dat moet worden toegewezen om de bewerking die wordt geretourneerd door te kunnen Toep assen @"microsoft.quantum.preparation.purifiedmixedstate" .

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a>Invoer

### <a name="targeterror--double"></a>targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)

De doel fout $ \epsilon $.


### <a name="ncoefficients--int"></a>nCoefficients: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal coëfficiënten dat moet worden opgegeven bij het voorbereiden van een gemengde status.



## <a name="output--mixedstatepreparationrequirements"></a>Uitvoer: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)

Een beschrijving van het aantal qubits dat in totaal is vereist en voor elk van de index-en garbage-registers die worden gebruikt door de @"microsoft.quantum.preparation.purifiedmixedstate" functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PurifiedMixedState](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)