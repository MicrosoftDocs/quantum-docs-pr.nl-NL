---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Bewerking ApplyIfElseRCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: dfd1c16a25a2da507024813a380386c8f4e49d30
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218747"
---
# <a name="applyifelserca-operation"></a>Bewerking ApplyIfElseRCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een van de twee unitary-bewerkingen toe, afhankelijk van de waarde van een klassiek resultaat.

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als er een resultaat `result` is gegeven, wordt de bewerking `zeroOp` met `zeroInput` als invoer toegepast wanneer deze `result` gelijk is aan `Zero` en wordt toegepast `oneOp(oneInput)` Wanneer `result == One` .

## <a name="input"></a>Invoer

### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Het meet resultaat dat wordt gebruikt om te bepalen `zeroOp` of het `oneOp` wordt toegepast.


### <a name="zeroop--t--unit--is-adj--ctl"></a>zeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De unitary-bewerking die moet worden toegepast wanneer `result == Zero` .


### <a name="zeroinput--t"></a>zeroInput: 'T

De invoer die moet worden opgegeven `zeroOp` als `result == Zero` .


### <a name="oneop--u--unit--is-adj--ctl"></a>oneOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De unitary-bewerking die moet worden toegepast wanneer `result == One` .


### <a name="oneinput--u"></a>oneInput: ' U

De invoer die moet worden opgegeven `oneOp` als `result == One` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking `zeroOp` die voorwaardelijk moet worden toegepast.
### <a name="u"></a>' U

Het invoer type van de bewerking `oneOp` die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Micro soft. Quantum. Canon. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Micro soft. Quantum. Canon. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Micro soft. Quantum. Canon. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Micro soft. Quantum. Canon. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)