---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Bewerking MeasureInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707173"
---
# <a name="measureinteger-operation"></a>Bewerking MeasureInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


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