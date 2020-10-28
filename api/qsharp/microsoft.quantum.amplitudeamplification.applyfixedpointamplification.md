---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Bewerking ApplyFixedPointAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707753"
---
# <a name="applyfixedpointamplification-operation"></a>Bewerking ApplyFixedPointAmplification

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Fixed-Point amplitude-versterkings algoritme

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="statepreporacle--stateoracle"></a>statePrepOracle: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Unitary Oracle waarmee de start status wordt voor bereid.


### <a name="startqubits--qubit"></a>startQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit registreren



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De startQubits moet de status $ \ket{0 \cdots 0} $ hebben. Met deze bewerking wordt een aantal query's herhaald in bevoegdheden van $2 $ totdat een maximum aantal query's is bereikt of de doel status is gevonden.