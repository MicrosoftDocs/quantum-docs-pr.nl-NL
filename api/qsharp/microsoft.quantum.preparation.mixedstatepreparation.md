---
uid: Microsoft.Quantum.Preparation.MixedStatePreparation
title: Door de gebruiker gedefinieerd MixedStatePreparation-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparation
qsharp.summary: Represents a particular mixed state that can be prepared on an index and a garbage register.
ms.openlocfilehash: 94d6483914b5d21bb51a5469c7123f834e9eb5da
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193570"
---
# <a name="mixedstatepreparation-user-defined-type"></a>Door de gebruiker gedefinieerd MixedStatePreparation-type

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dit object vertegenwoordigt een bepaalde gemengde status die kan worden voor bereid op een index en een garbagecollection-registratie.

```qsharp

newtype MixedStatePreparation = (Requirements : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements, Norm : Double, Prepare : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benoemde items

### <a name="requirements--mixedstatepreparationrequirements"></a>Vereisten: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)


### <a name="norm--double"></a>Norm: [dubbel](xref:microsoft.quantum.lang-ref.double)


### <a name="prepare--littleendianqubitqubit--unit--is-adj--ctl"></a>Voorbereiden: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. PurifiedMixedState](xref:Microsoft.Quantum.PurifiedMixedState)