---
uid: Microsoft.Quantum.Canon.BoundC
title: De functie BoundC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207578"
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

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)