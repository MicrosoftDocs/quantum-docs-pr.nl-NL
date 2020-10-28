---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Bewerking DecodeFromSteaneCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e6831a8630c0a80c2abe7c4a720263f0de03edc4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702518"
---
# <a name="decodefromsteanecode-operation"></a>Bewerking DecodeFromSteaneCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Een inverse coderings bewerking waarbij een niet-versleutelde Quantum-REGI ster wordt toegewezen aan een gecodeerd Quantum REGI ster onder de Quantum code ⟦, 1, 3 ⟧ Steane.

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Invoer

### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met qubits die de code ring logische status van 5 Qubit vertegenwoordigt.



## <a name="output--qubitqubit"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Een Qubit-matrix van lengte 1 die de niet-versleutelde status in de eerste para meter weergeeft, samen met de hulp qubits in de tweede para meter.

## <a name="remarks"></a>Opmerkingen

De gekozen decoder maakt gebruik van de CSS-code-eigenschap van de ⟦-code van de 7, 1, 3 ⟧ Steane, dat wil zeggen, het corrigeert X fouten en Z-fouten afzonderlijk. Een eigenschap van de code is dat de locatie van de X, respectievelijk de Z-correctie die moet worden toegepast, de 3-bits code ring van de X, respectievelijk Z Syndrome is als een geheel getal.

## <a name="references"></a>Naslaginformatie

- D. Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. SteaneCodeEncoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [Micro soft. Quantum. ErrorCorrection. SteaneCodeDecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)