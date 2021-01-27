---
uid: Microsoft.Quantum.Canon.BoundCA
title: De functie BoundCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844520"
---
# <a name="boundca-function"></a>De functie BoundCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.
De wijzigings functie `CA` geeft aan dat alle bewerkingen in de matrix adjointable en bewerkbaar zijn.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="operations--t--unit--is-adj--ctl"></a>bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []

Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.



## <a name="output--t--unit--is-adj--ctl"></a>Output: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de bewerkingen in de matrix Act.

## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

en

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)