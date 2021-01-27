---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Bewerking CompareGTSI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846694"
---
# <a name="comparegtsi-operation"></a>Bewerking CompareGTSI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Wrapper voor ondertekende integer-vergelijking: `result = xs > ys` .

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="xs--signedlittleendian"></a>XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Eerste $n $-bits nummer


### <a name="ys--signedlittleendian"></a>kalenderda: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Tweede $n $-bits nummer


### <a name="result--qubit"></a>resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Wordt gespiegeld als $xs > kalenderda $



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

