---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Bewerking RecoverCSS
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: 48d3cd3d5f6aea265fac2f50b913ab855a31accf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702423"
---
# <a name="recovercss-operation"></a>Bewerking RecoverCSS

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Voert één afronding van de fout correctie uit op basis van een Quantum code die wordt beschreven door een `CSS` type.

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Invoer

### <a name="code--css"></a>code: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Een Quantum CSS-fout: de code die is verpakt als een `CSS` type wordt beschreven in een beschrijving van de code ring en het decoderen van Quantum gegevens en hoe fout-Syndromes worden gemeten.


### <a name="fnx--recoveryfn"></a>fnX: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Een `RecoveryFn` waarmee elke $X $ error Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.


### <a name="fnz--recoveryfn"></a>fnZ: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Een `RecoveryFn` waarmee elke $Z $ error Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [Micro soft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)