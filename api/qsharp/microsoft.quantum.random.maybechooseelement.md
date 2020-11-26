---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192856"
---
# <a name="maybechooseelement-operation"></a>Bewerking MaybeChooseElement

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Op basis van een matrix met gegevens en een distributie over de indices probeert een wille keurig element te kiezen.

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a>Invoer

### <a name="data--t"></a>gegevens: ' []

De matrix waaruit een element moet worden gekozen.


### <a name="indexdistribution--discretedistribution"></a>indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Een distributie over de indices van `data` .



## <a name="output--boolt"></a>Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

