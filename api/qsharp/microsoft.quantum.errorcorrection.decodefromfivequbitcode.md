---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Bewerking DecodeFromFiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 421da6296b604f30aefed58730091f64f19c3a61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702537"
---
# <a name="decodefromfivequbitcode-operation"></a>Bewerking DecodeFromFiveQubitCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Decodeert de ⟦ van 5, 1, 3 en ⟧.

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Invoer

### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met qubits die de code ring logische status van 5 Qubit vertegenwoordigt.



## <a name="output--qubitqubit"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Een Qubit-matrix van lengte 1 die de niet-versleutelde status in de eerste para meter weergeeft, samen met de hulp qubits in de tweede para meter.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. FiveQubitCodeEncoder](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)