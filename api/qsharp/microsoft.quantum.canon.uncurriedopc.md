---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: De functie UncurriedOpC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 05df99dce8b167f32078ce256748647ceb94d0fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851991"
---
# <a name="uncurriedopc-function"></a>De functie UncurriedOpC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.
De aanpassings functie `C` geeft aan dat de bewerkingen kunnen worden bestuurd.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit--is-ctl"></a>curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit--is-ctl"></a>Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste argument van een Curried-functie.
### <a name="u"></a>' U

Het type van het tweede argument van een Curried-functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)