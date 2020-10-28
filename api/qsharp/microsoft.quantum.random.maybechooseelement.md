---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707866"
---
# <a name="maybechooseelement-operation"></a>Bewerking MaybeChooseElement

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


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

