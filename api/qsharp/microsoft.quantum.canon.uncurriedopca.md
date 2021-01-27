---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: De functie UncurriedOpCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 910d8a3006a2f217888b791e479e10f9f1a6965e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840044"
---
# <a name="uncurriedopca-function"></a>De functie UncurriedOpCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.
De aanpassings functie `CA` geeft aan dat de bewerkingen kunnen worden bestuurd en adjointable.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit--is-adj--ctl"></a>curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit--is-adj--ctl"></a>Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste argument van een Curried-functie.
### <a name="u"></a>' U

Het type van het tweede argument van een Curried-functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)