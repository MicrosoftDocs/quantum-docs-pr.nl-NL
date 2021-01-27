---
uid: Microsoft.Quantum.Canon.CurriedOp
title: De functie CurriedOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840767"
---
# <a name="curriedop-function"></a>De functie CurriedOp

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een Curried-versie van een bewerking op twee invoer.

Op basis van een bewerking met twee invoer, past deze functie de isomorphism $f van Curry (x, y) \equiv f (x) (y) $ om een bewerking te retour neren van één invoer waarmee een bewerking van één invoer wordt geretourneerd.

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a>Invoer

### <a name="op--tu--unit"></a>op: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking waarvan de invoer een paar is.



## <a name="output--t---u--unit"></a>Uitvoer: niet-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die het eerste element van een paar accepteert en een bewerking retourneert die de invoer accepteert van het tweede element van de invoer van de oorspronkelijke bewerking.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste onderdeel van een functie die op paren is gedefinieerd.
### <a name="u"></a>' U

Het type van het tweede onderdeel van een functie die op paren is gedefinieerd.

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```