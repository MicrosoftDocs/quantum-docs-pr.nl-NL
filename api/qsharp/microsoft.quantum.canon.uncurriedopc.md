---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: De functie UncurriedOpC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703713"
---
# <a name="uncurriedopc-function"></a>De functie UncurriedOpC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.
De aanpassings functie `C` geeft aan dat de bewerkingen kunnen worden bestuurd.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit-ctl"></a>curriedOp: 'T-> ' U => CTL van de [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit-ctl"></a>Output: ('T, ' U) => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste argument van een Curried-functie.
### <a name="u"></a>' U

Het type van het tweede argument van een Curried-functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)