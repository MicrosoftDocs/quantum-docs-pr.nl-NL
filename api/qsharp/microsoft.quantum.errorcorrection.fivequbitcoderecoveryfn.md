---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: De functie FiveQubitCodeRecoveryFn
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702477"
---
# <a name="fivequbitcoderecoveryfn-function"></a>De functie FiveQubitCodeRecoveryFn

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Retourneert een functie die fout Syndrome-metingen toewijst aan de juiste fout: Pauli Opera tors worden door de zoek opdracht voor de ⟦ 5, 1, 3 ⟧ Quantum code toegewezen.

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Functie van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` Opera tors retourneert die de gedetecteerde fout corrigeert.

## <a name="remarks"></a>Opmerkingen

Door alle fouten van gewicht $1 $ te herhalen, krijgen we $3 \ Times 5 = 15 $ mogelijk niet-trivial Syndromes.
Samen met de identiteit wordt een tabel met fouten en bijbehorende Syndrome gebouwd. Voor de 5 Qubit-code wordt deze tabel gegeven door: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ met $Y _I $ verkregen door de $X _I $ en $Z _I $ Syndromes toe te voegen. Houd er rekening mee dat de volg orde in het herstel van de tabel zoek opdracht wordt gegeven door de bitvectors te converteren naar gehele getallen (met behulp van little endian).

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)