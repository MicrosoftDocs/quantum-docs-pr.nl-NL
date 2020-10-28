---
uid: Microsoft.Quantum.Bitwise.XBits
title: De functie XBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 91619803c7efe56e617b16637f5302aa0b7978ec
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705572"
---
# <a name="xbits-function"></a>De functie XBits

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket [](https://nuget.org/packages/)


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