---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Bewerking DecodeFromSteaneCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 54e47b65ed7a89c8ff9026126a9542d3d7ba15cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827392"
---
# <a name="decodefromsteanecode-operation"></a>Bewerking DecodeFromSteaneCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="references"></a>Verwijzingen

- D. Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. SteaneCodeEncoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [Micro soft. Quantum. ErrorCorrection. SteaneCodeDecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)