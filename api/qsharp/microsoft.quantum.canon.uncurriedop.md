---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: De functie UncurriedOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: d707b52bb17f4dea795fa4ff824c785e506b8b20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852009"
---
# <a name="uncurriedop-function"></a>De functie UncurriedOp

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a>Invoer

### <a name="curriedop--t---u--unit"></a>curriedOp: 'T-> ' U =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een functie waarmee bewerkingen worden geretourneerd.



## <a name="output--tu--unit"></a>Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de eerste invoer voor een Curried-bewerking.
### <a name="u"></a>' U

Het type van de tweede invoer voor een Curried-bewerking.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. UncurriedOpC](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [Micro soft. Quantum. Canon. UncurriedOpA](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [Micro soft. Quantum. Canon. UncurriedOpCA](xref:Microsoft.Quantum.Canon.UncurriedOpCA)