---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: De functie SteaneCodeRecoveryFns
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: b1dd1c2e9a71e58bd8a86d1759a8b6af13a49614
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702398"
---
# <a name="steanecoderecoveryfns-function"></a>De functie SteaneCodeRecoveryFns

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Decoder voor gecombineerde X-en Z-onderdelen van de stabilisatoren groep van de ⟦-⟧ Steane Quantum-code.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>Uitvoer: ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

De tuple van de functies van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` bewerkingen retourneert die de gedetecteerde fout corrigeren.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryX](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryZ](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)