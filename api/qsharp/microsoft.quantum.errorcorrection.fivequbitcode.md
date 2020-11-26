---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: De functie FiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200880"
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