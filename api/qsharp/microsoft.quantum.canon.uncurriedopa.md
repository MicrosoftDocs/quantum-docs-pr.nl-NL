---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: De functie UncurriedOpA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703718"
---
# <a name="uncurriedopa-function"></a>De functie UncurriedOpA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.
De aanpassings functie `A` geeft aan dat de bewerkingen adjointable zijn.

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit-adj"></a>curriedOp: 'T-> ' U => correctie van de [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit-adj"></a>Output: ('T, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste argument van een Curried-functie.
### <a name="u"></a>' U

Het type van het tweede argument van een Curried-functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)