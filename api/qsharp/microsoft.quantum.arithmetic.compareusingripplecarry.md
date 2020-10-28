---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Bewerking CompareUsingRippleCarry
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: 842e7ded1e38f4f6e01e79d2758e30afb85dd349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707380"
---
# <a name="compareusingripplecarry-operation"></a>Bewerking CompareUsingRippleCarry

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Met deze bewerking wordt getest of een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits groter is dan een ander geheel getal, waarbij een XOR van het resultaat wordt toegepast op een uitvoer Qubit.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit
```


## <a name="description"></a>Beschrijving

Als er twee gehele getallen zijn opgegeven `x` en `y` zijn opgeslagen in Qubit-registers met een gelijke grootte, controleert deze bewerking of ze voldoen `x > y` . Als deze waarde True is, wordt 1 XORed in een uitvoer Qubit. Anders wordt 0 XORed in een uitvoer Qubit.
Met andere woorden, deze bewerking kan worden weer gegeven door de unitary $ $ \begin{align} U\ket {x} \ Ket {y} \ Ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="x--littleendian"></a>x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het eerste getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.


### <a name="y--littleendian"></a>y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het tweede getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.


### <a name="output--qubit"></a>uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit waarin het resultaat van de vergelijking wordt opgeslagen $x>y $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- Een nieuwe Quantum rimpel: Voeg circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184