---
uid: Microsoft.Quantum.Bitwise.XBits
title: De functie XBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845236"
---
# <a name="xbits-function"></a>De functie XBits

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert een geheel getal dat de X-bits van een matrix van Pauli-Opera tors vertegenwoordigt.

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een matrix met Pauli-Opera tors die moeten worden weer gegeven als een geheel getal.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal $x $ met binaire weer gave $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, waarbij $p _I = $0 als `paulis[i]` is `PauliI` of en de $p `PauliZ` _I = $1 als dat zo `paulis[i]` is `PauliX` of `PauliY` .

## <a name="remarks"></a>Opmerkingen

De functie wordt gegenereerd als de lengte van de `paulis` matrix groter is dan 63.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. bitsgewijze. ZBits](xref:Microsoft.Quantum.Bitwise.ZBits)