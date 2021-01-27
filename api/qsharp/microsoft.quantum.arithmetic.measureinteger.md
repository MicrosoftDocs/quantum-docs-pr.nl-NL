---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Bewerking MeasureInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843108"
---
# <a name="measureinteger-operation"></a>Bewerking MeasureInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de inhoud van een Quantum register gemeten en omgezet in een geheel getal. De meting wordt uitgevoerd met betrekking tot de standaard berekening, d.w.z. de eigenbasis van `PauliZ` .

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>Invoer

### <a name="target--littleendian"></a>doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register in de code ring met little endian.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een niet-ondertekend geheel getal dat de gemeten waarde van bevat `target` .

## <a name="remarks"></a>Opmerkingen

Met deze bewerking wordt de invoer register opnieuw ingesteld op de status $ \ket{00\cdots 0} $, die geschikt is om terug te gaan naar een doel machine.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. MeasureIntegerBE](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)