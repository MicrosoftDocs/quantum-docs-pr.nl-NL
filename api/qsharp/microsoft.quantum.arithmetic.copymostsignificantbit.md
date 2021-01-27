---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Bewerking CopyMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843271"
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