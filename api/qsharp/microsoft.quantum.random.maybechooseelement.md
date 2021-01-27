---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856119"
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



## <a name="example"></a>Voorbeeld

De volgende letter Q # fragment kiest een wille keurig element uit een matrix:

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```