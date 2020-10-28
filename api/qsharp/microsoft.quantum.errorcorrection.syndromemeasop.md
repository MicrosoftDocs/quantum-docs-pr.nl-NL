---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Door de gebruiker gedefinieerd SyndromeMeasOp-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702387"
---
# <a name="syndromemeasop-user-defined-type"></a>Door de gebruiker gedefinieerd SyndromeMeasOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bewerking aangeduid die wordt gebruikt om de Syndrome van een fout-correct code blok te meten.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Opmerkingen

De hand tekening `(LogicalRegister => Syndrome)` vertegenwoordigt een bewerking die gezamenlijk werkt op de qubits in `LogicalRegister` en een aantal hulp qubits, gevolgd door een meting van de hulp qubits om een waarde op te halen `Syndrome` die `Result[]` van deze metingen is.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Micro soft. Quantum. ErrorCorrection. Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)