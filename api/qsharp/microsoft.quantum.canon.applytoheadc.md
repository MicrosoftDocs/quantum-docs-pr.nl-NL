---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Bewerking ApplyToHeadC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 2b7321a6c385e2d98a0e91a8f58091ea8dc43ff4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208598"
---
# <a name="applytoheadc-operation"></a>Bewerking ApplyToHeadC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op het eerste element van een matrix.

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Beschrijving

Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

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
- [Micro soft. Quantum. Canon. ApplyToHeadCA](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)