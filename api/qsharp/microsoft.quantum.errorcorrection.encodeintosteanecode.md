---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Bewerking EncodeIntoSteaneCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 39b8ab549413d9d5281f6b84a6e970c45242fca8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702506"
---
# <a name="encodeintosteanecode-operation"></a>Bewerking EncodeIntoSteaneCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Een coderings bewerking waarbij een niet-versleutelde Quantum wordt toegewezen aan een versleuteld Quantum REGI ster onder de Quantum code ⟦, 1, 3 ⟧ Steane.

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Invoer

### <a name="physregister--qubit"></a>physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-REGI ster dat de niet-versleutelde Quantum status bevat


### <a name="auxqubits--qubit"></a>auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-REGI ster dat in eerste instantie nul is en dat wordt toegevoegd aan het Quantum systeem zodat een coderings bewerking kan worden uitgevoerd



## <a name="output--logicalregister"></a>Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een Quantum registreert de status nadat het Steane-coderings programma is toegepast

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Micro soft. Quantum. ErrorCorrection. SteaneCodeDecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)