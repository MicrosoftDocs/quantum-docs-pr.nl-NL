---
uid: Microsoft.Quantum.Bitwise.ZBits
title: De functie ZBits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219444"
---
# <a name="zbits-function"></a>De functie ZBits

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert een geheel getal dat de Z-bits van een matrix van Pauli-Opera tors vertegenwoordigt.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een matrix met Pauli-Opera tors die moeten worden weer gegeven als een geheel getal.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal $x $ met binaire weer gave $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, waarbij $p _I = $0 als `paulis[i]` is `PauliI` of en de $p `PauliX` _I = $1 als dat zo `paulis[i]` is `PauliY` of `PauliZ` .

## <a name="remarks"></a>Opmerkingen

De functie wordt gegenereerd als de lengte van de `paulis` matrix groter is dan 63.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. bitsgewijze. XBits](xref:Microsoft.Quantum.Bitwise.XBits)