---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Door de gebruiker gedefinieerd ControlledRotation-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702063"
---
# <a name="controlledrotation-user-defined-type"></a>Door de gebruiker gedefinieerd ControlledRotation-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Beschrijft een beheerde rotatie in termen van de doel-en besturings indexen, rotatieas en index in een model parameter vector.

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="targetindex--int"></a>TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)

Index van de doel-Qubit voor deze beheerde rotatie.
### <a name="controlindices--int"></a>ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix van het besturings element Qubit Indexes voor deze draaiing.
### <a name="axis--pauli"></a>As: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

De as voor deze draaiing.
### <a name="parameterindex--int"></a>ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)

Een index in een model parameter vector waarmee de hoek voor deze draaiing wordt beschreven.

## <a name="remarks"></a>Opmerkingen

Een onbeheerde rotatie kan worden weer gegeven door `ControlIndices` in te stellen op een lege matrix met indexen, `new Int[0]` .