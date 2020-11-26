---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Door de gebruiker gedefinieerd ControlledRotation-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 1e664b470caeba656ea4a73f70bbc0ef5fe76f7e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196562"
---
# <a name="controlledrotation-user-defined-type"></a>Door de gebruiker gedefinieerd ControlledRotation-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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