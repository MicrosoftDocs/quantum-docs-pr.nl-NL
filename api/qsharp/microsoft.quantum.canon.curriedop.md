---
uid: Microsoft.Quantum.Canon.CurriedOp
title: De functie CurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704284"
---
# <a name="curriedop-function"></a>De functie CurriedOp

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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