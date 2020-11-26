---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Bewerking ApplyToElementCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 8ae4ece0d3d56ea2be1ce494ab0c5ee7caacbbf8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208853"
---
# <a name="applytoelementca-operation"></a>Bewerking ApplyToElementCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-adj--ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die moet worden toegepast.


### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)

Een index in de matrix met doelen.


### <a name="targets--t"></a>doelen: ' []

Een matrix met mogelijke doelen voor `op` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToElement](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [Micro soft. Quantum. Canon. ApplyToElementC](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Micro soft. Quantum. Canon. ApplyToElementA](xref:Microsoft.Quantum.Canon.ApplyToElementA)