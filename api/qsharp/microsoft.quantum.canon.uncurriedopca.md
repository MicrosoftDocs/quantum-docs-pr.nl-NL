---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: De functie UncurriedOpCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703712"
---
# <a name="uncurriedopca-function"></a>De functie UncurriedOpCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.
De aanpassings functie `CA` geeft aan dat de bewerkingen kunnen worden bestuurd en adjointable.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit-ctl--adj"></a>curriedOp: 'T-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit-ctl--adj"></a>Output: ('T, ' U) => van CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) en correctie

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste argument van een Curried-functie.
### <a name="u"></a>' U

Het type van het tweede argument van een Curried-functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)