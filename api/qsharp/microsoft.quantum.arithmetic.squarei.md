---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Bewerking SquareI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: d7334d50f245ba358624e6e2eee94b63d9ed7569
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706221"
---
# <a name="squarei-operation"></a>Bewerking SquareI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Berekent het kwadraat van het gehele getal `xs` in `result` , die in eerste instantie nul moet zijn.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bits nummer naar vier kant (LittleEndian)


### <a name="result--littleendian"></a>resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Maakt gebruik van een standaard methode voor Shift en toevoegen om het kwadraat te berekenen. Slaat $n-$1 qubits op vergeleken met de oplossing voor rechtse, die eerst XS kopieert voordat een gewone vermenigvuldiger wordt toegepast en vervolgens de Kopieer bewerking ongedaan wordt.