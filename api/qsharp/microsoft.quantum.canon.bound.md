---
uid: Microsoft.Quantum.Canon.Bound
title: Gebonden functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207595"
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

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. BoundC](xref:Microsoft.Quantum.Canon.BoundC)
- [Micro soft. Quantum. Canon. Bounda](xref:Microsoft.Quantum.Canon.BoundA)
- [Micro soft. Quantum. Canon. BoundCA](xref:Microsoft.Quantum.Canon.BoundCA)