---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Bewerking ApplyToHeadCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208547"
---
# <a name="applytoheadca-operation"></a>Bewerking ApplyToHeadCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op het eerste element van een matrix.

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-adj--ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die moet worden toegepast.


### <a name="targets--t"></a>doelen: ' []

Een matrix met doelen waarop de eerste wordt toegepast `op` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToHead](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [Micro soft. Quantum. Canon. ApplyToHeadA](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [Micro soft. Quantum. Canon. ApplyToHeadC](xref:Microsoft.Quantum.Canon.ApplyToHeadC)