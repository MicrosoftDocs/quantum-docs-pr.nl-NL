---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Door de gebruiker gedefinieerd ControlledRotation-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847395"
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

## <a name="example"></a>Voorbeeld

Hieronder vindt u een rotatie over de $X $-as van de eerste Qubit in een REGI ster, dat wordt gecontroleerd op de tweede Qubit en met een hoek die wordt gegeven door de vierde para meter in een sequentieel model:

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a>Opmerkingen

Een onbeheerde rotatie kan worden weer gegeven door `ControlIndices` in te stellen op een lege matrix met indexen, `new Int[0]` .