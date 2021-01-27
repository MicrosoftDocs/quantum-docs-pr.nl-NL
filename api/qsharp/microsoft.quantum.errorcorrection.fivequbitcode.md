---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: De functie FiveQubitCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853144"
---
# <a name="fivequbitcode-function"></a>De functie FiveQubitCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een QECC-waarde die de ⟦ 5, 1, 3 ⟧ code encoder en de decoder met in-place Syndrome meting.

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a>Uitvoer: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Retourneert een implementatie van een Quantum fout correctie code door een type op te geven `QECC` .

## <a name="remarks"></a>Opmerkingen

Deze code is onafhankelijk van de volgende twee documenten gevonden:

- C. HxBxD. Bennett,, D. DiVincenzo, J. A. Smolin en W. K. Wootters, "gemengde status entanglement en Quantum fout correctie," fysiek. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 en
- N. LaFlamme, C. Miquel, J. P. Paz en W. H. Zurek, "perfecte Quantum fout correctie code," fysiek. Rev. lett. 77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019