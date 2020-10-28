---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Herstel bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702428"
---
# <a name="recover-operation"></a>Herstel bewerking

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Voert één afronding van de fout correctie uit op basis van een Quantum code die wordt beschreven door een `QECC` type.

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Invoer

### <a name="code--qecc"></a>code: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Een Quantum fout: een code die is verpakt als `QECC` type, beschrijft de code ring en de code ring van Quantum gegevens en hoe fout-Syndromes worden gemeten.


### <a name="fn--recoveryfn"></a>FN: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Een `RecoveryFn` waarmee elke fout Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [Micro soft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)