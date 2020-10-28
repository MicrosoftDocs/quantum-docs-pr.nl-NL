---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Bewerking DecodeFromBitFlipCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702543"
---
# <a name="decodefrombitflipcode-operation"></a>Bewerking DecodeFromBitFlipCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Decoderen van de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-Flip code.

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Invoer

### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een code blok van de bits-Flip-code.



## <a name="output--qubitqubit"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Een tuple van de gegevens die zijn gecodeerd in het logische REGI ster en de hulp qubits die wordt gebruikt om de Syndrome aan te duiden.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Micro soft. Quantum. ErrorCorrection. EncodeIntoBitFlipCode](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)