---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Bewerking AssertMostSignificantBit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707452"
---
# <a name="assertmostsignificantbit-operation"></a>Bewerking AssertMostSignificantBit

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Beweringen dat de meest significante Qubit van een Qubit-REGI ster die een niet-ondertekend geheel getal vertegenwoordigt, zich in een bepaalde staat bevindt.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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