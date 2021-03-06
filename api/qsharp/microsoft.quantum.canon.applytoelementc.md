---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Bewerking ApplyToElementC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850748"
---
# <a name="applytoelementc-operation"></a>Bewerking ApplyToElementC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Beschrijving

Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

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
- [Micro soft. Quantum. Canon. ApplyToElementA](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [Micro soft. Quantum. Canon. ApplyToElementCA](xref:Microsoft.Quantum.Canon.ApplyToElementCA)