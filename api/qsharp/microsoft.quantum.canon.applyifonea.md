---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Bewerking ApplyIfOneA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 200908f2958b74e4823c891ef901474d75d18336
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218543"
---
# <a name="applyifonea-operation"></a>Bewerking ApplyIfOneA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een adjointable-bewerking toegepast op een klassieke resultaat waarde die één.

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a>Beschrijving

`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` . Als `Zero` , gebeurt er niets met `target` .
Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.

## <a name="input"></a>Invoer

### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Een meet resultaat dat bepaalt of op wordt toegepast of niet.


### <a name="op--t--unit--is-adj"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie

Een bewerking die voorwaardelijk moet worden toegepast.


### <a name="target--t"></a>doel: 'T

De invoer waarop de bewerking wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyIfOneC](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [Micro soft. Quantum. Canon. ApplyIfOneA](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [Micro soft. Quantum. Canon. ApplyIfOneCA](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)