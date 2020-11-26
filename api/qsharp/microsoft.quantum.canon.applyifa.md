---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Bewerking ApplyIfA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: d2880bbb95ebaf621ef9e5885051b94f32a3f1cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218764"
---
# <a name="applyifa-operation"></a>Bewerking ApplyIfA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een adjointable bewerking toegepast die is voor bereid op een klassieke bit.

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a>Beschrijving

Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde. Als `false` , gebeurt er niets met `target` .
Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-adj"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie

Een bewerking die voorwaardelijk moet worden toegepast.


### <a name="bit--bool"></a>bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)

een Booleaanse waarde die bepaalt of op wordt toegepast of niet.


### <a name="target--t"></a>doel: 'T

De invoer waarop de bewerking wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyIfC](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Micro soft. Quantum. Canon. ApplyIfA](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Micro soft. Quantum. Canon. ApplyIfCA](xref:Microsoft.Quantum.Canon.ApplyIfCA)