---
uid: Microsoft.Quantum.Canon.BoundCA
title: De functie BoundCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704436"
---
# <a name="boundca-function"></a>De functie BoundCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.
De wijzigings functie `CA` geeft aan dat alle bewerkingen in de matrix adjointable en bewerkbaar zijn.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="operations--t--unit-adj--ctl"></a>bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []

Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.



## <a name="output--t--unit-adj--ctl"></a>Output: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de bewerkingen in de matrix Act.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)