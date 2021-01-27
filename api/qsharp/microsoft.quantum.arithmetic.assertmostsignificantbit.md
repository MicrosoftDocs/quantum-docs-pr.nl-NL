---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Bewerking AssertMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843429"
---
# <a name="assertmostsignificantbit-operation"></a>Bewerking AssertMostSignificantBit

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Beweringen dat de meest significante Qubit van een Qubit-REGI ster die een niet-ondertekend geheel getal vertegenwoordigt, zich in een bepaalde staat bevindt.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="value--__invalidresult__"></a>waarde: __ongeldig <Result>__

De waarde van de hoogste bit die wordt bevestigd.


### <a name="number--littleendian"></a>nummer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Niet-ondertekende integer waarvan de hoogste bit wordt gecontroleerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De gecontroleerde versie van deze bewerking negeert besturings elementen.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. intrinsiek. assert](xref:Microsoft.Quantum.Intrinsic.Assert)