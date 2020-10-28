---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Bewerking EncodeIntoFiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702507"
---
# <a name="encodeintofivequbitcode-operation"></a>Bewerking EncodeIntoFiveQubitCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Codeert in de ⟦ van 5, 1, 3 en ⟧.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Invoer

### <a name="physregister--qubit"></a>physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit die een niet-gecodeerde status voor stelt. Deze matrix `Qubit[]` heeft de lengte 1.


### <a name="auxqubits--qubit"></a>auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster met hulp qubits die wordt gebruikt om de gecodeerde status voor te stellen.



## <a name="output--logicalregister"></a>Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met fysieke qubits van `LogicalRegister` het type dat de gecodeerde status opslaat.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)