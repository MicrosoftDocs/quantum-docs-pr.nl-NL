---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Bewerking GreaterThan
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 644d68affbdb508938f76de5025a1a463e7284e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223082"
---
# <a name="greaterthan-operation"></a>Bewerking GreaterThan

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een groter-dan-vergelijking toe tussen twee gehele getallen die zijn gecodeerd in Qubit-journalen, waarbij een doel-Qubit wordt gespiegeld op basis van het resultaat van de vergelijking.

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Voert een strikt groter dan vergelijking van twee gehele getallen uit $x $ en $y $, gecodeerd in Qubit registreert XS en kalenderda. Als $x > y $, wordt het resultaat Qubit gespiegeld, anders behoudt het resultaat Qubit de status.

## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit Registreer Codeer de eerste integer $x $.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit Registreer code ring de tweede integer $y $.


### <a name="result--qubit"></a>resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eén Qubit die wordt gespiegeld als $x > y $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Maakt gebruik van de slag die $x-y = (x ' + y) ' $, waarbij ' de complement vormt.

## <a name="references"></a>Referenties

- Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1

- Thomas Haener, Martin Roetteler, Krysta M. Svore: "factoring met behulp van 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging", 2016 https://arxiv.org/abs/1611.07995