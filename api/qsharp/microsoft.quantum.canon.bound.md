---
uid: Microsoft.Quantum.Canon.Bound
title: Gebonden functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841055"
---
# <a name="bound-function"></a>Gebonden functie

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a>Invoer

### <a name="operations--t--unit-"></a>bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []

Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.



## <a name="output--t--unit"></a>Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de bewerkingen in de matrix Act.

## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
let bound = Bound([U, V]);
bound(x);
```

en

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. BoundC](xref:Microsoft.Quantum.Canon.BoundC)
- [Micro soft. Quantum. Canon. Bounda](xref:Microsoft.Quantum.Canon.BoundA)
- [Micro soft. Quantum. Canon. BoundCA](xref:Microsoft.Quantum.Canon.BoundCA)