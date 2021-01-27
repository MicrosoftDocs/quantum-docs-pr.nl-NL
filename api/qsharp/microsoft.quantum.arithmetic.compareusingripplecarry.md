---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Bewerking CompareUsingRippleCarry
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: ce2be140ecfed21dea6212651249b4a11d2542c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843294"
---
# <a name="compareusingripplecarry-operation"></a>Bewerking CompareUsingRippleCarry

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Met deze bewerking wordt getest of een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits groter is dan een ander geheel getal, waarbij een XOR van het resultaat wordt toegepast op een uitvoer Qubit.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
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



## <a name="references"></a>Verwijzingen

- Een nieuwe Quantum rimpel: Voeg circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184