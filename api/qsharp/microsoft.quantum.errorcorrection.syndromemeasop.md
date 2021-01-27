---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Door de gebruiker gedefinieerd SyndromeMeasOp-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 36336f9e47e5f360cf5e19ffb6e15b4af88b2580
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850053"
---
# <a name="syndromemeasop-user-defined-type"></a>Door de gebruiker gedefinieerd SyndromeMeasOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking aangeduid die wordt gebruikt om de Syndrome van een fout-correct code blok te meten.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a>Voorbeeld

Meet Syndromes voor de bits-Flip code $S = \langle ZZI, IZZ \rangle $ lege qubits op een niet-fout tolerante manier:

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a>Opmerkingen

De hand tekening `(LogicalRegister => Syndrome)` vertegenwoordigt een bewerking die gezamenlijk werkt op de qubits in `LogicalRegister` en een aantal hulp qubits, gevolgd door een meting van de hulp qubits om een waarde op te halen `Syndrome` die `Result[]` van deze metingen is.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Micro soft. Quantum. ErrorCorrection. Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)