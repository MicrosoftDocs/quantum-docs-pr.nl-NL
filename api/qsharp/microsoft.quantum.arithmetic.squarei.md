---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Bewerking SquareI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846316"
---
# <a name="squarei-operation"></a>Bewerking SquareI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Berekent het kwadraat van het gehele getal `xs` in `result` , die in eerste instantie nul moet zijn.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bits nummer naar vier kant (LittleEndian)


### <a name="result--littleendian"></a>resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Maakt gebruik van een standaard methode voor Shift en toevoegen om het kwadraat te berekenen. Slaat $n-$1 qubits op vergeleken met de oplossing voor rechtse, die eerst XS kopieert voordat een gewone vermenigvuldiger wordt toegepast en vervolgens de Kopieer bewerking ongedaan wordt.