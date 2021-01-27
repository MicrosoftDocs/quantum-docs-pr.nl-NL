---
uid: Microsoft.Quantum.Canon.BoundC
title: De functie BoundC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 6b640c0dab14778336f42098e699e7e68cc726df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841045"
---
# <a name="boundc-function"></a>De functie BoundC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.
De wijzigings functie `C` geeft aan dat alle bewerkingen in de matrix kunnen worden bestuurd.

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="operations--t--unit--is-ctl"></a>bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL []

Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.



## <a name="output--t--unit--is-ctl"></a>Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de bewerkingen in de matrix Act.

## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
let bound = BoundC([U, V]);
bound(x);
```

en

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)