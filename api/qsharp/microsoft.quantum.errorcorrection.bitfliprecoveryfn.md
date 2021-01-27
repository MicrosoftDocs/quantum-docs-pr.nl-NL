---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: De functie BitFlipRecoveryFn
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: 1cf2bd944b4dcaadeeca96fa0f576250590962e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827601"
---
# <a name="bitfliprecoveryfn-function"></a>De functie BitFlipRecoveryFn

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Functie voor herstel Pauli bewerkingen voor de gegeven Syndrome meting door de opzoek tabel voor de ⟦ 3, 1, 1 ⟧ bits.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Functie van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` bewerkingen retourneert die de gedetecteerde fout corrigeert.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)