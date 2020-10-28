---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Bewerking EncodeIntoBitFlipCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 694d3f7a412b64b0ad533b4478a9274384d05c61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702512"
---
# <a name="encodeintobitflipcode-operation"></a>Bewerking EncodeIntoBitFlipCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Hiermee wordt gecodeerd in de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bits-Flip code.

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Invoer

### <a name="physregister--qubit"></a>physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van fysieke qubits die de gegevens vertegenwoordigen die moeten worden beveiligd.


### <a name="auxqubits--qubit"></a>auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van de hulp qubits in eerste instantie in de $ \ket {00} $-status die moet worden gebruikt bij het coderen van de gegevens die moeten worden beveiligd.



## <a name="output--logicalregister"></a>Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

De fysieke en hulp qubits die worden gebruikt in de code ring, weer gegeven als een logisch REGI ster.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)