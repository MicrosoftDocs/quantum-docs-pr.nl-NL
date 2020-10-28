---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: De functie BitFlipRecoveryFn
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: dad90475b2506187282825e143b11adc5120f453
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702549"
---
# <a name="bitfliprecoveryfn-function"></a>De functie BitFlipRecoveryFn

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Functie voor herstel Pauli bewerkingen voor de gegeven Syndrome meting door de opzoek tabel voor de ⟦ 3, 1, 1 ⟧ bits.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Functie van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` bewerkingen retourneert die de gedetecteerde fout corrigeert.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)