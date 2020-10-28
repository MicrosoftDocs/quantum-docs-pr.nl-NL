---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: De functie FiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 7509de880b1e3ea8964b61e4b3f034ce20b2f202
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702483"
---
# <a name="fivequbitcode-function"></a>De functie FiveQubitCode

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


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