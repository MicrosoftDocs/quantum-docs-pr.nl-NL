---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Bewerking CopyMostSignificantBit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 39a2dc2fe33f46c2767def06a44cde07e2f01497
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223286"
---
# <a name="copymostsignificantbit-operation"></a>Bewerking CopyMostSignificantBit

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de meest significante bit van een Qubit-REGI ster gekopieerd `from` die een niet-ondertekend geheel getal vertegenwoordigt in de Qubit `target` .

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="from--littleendian"></a>van: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het niet-ondertekende integer waarvan de hoogste bit wordt gekopieerd.
het gehele getal is gecodeerd in de indeling little endian.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De Qubit waarin de hoogste bit wordt gekopieerd. De bits code ring wordt berekend op basis van de berekening.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)