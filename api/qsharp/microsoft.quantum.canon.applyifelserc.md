---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: Bewerking ApplyIfElseRC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: bac763168dbc7379691f850a79cbb6e61639ba89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841790"
---
# <a name="applyifelserc-operation"></a>Bewerking ApplyIfElseRC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een van de twee instel bare bewerkingen toe, afhankelijk van de waarde van een klassiek resultaat.

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit is Ctl
```


## <a name="description"></a>Beschrijving

Als er een resultaat `result` is gegeven, wordt de bewerking `zeroOp` met `zeroInput` als invoer toegepast wanneer deze `result` gelijk is aan `Zero` en wordt toegepast `oneOp(oneInput)` Wanneer `result == One` .

## <a name="input"></a>Invoer

### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Het meet resultaat dat wordt gebruikt om te bepalen `zeroOp` of het `oneOp` wordt toegepast.


### <a name="zeroop--t--unit--is-ctl"></a>zeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

De instelbaar bewerking die moet worden toegepast wanneer `result == Zero` .


### <a name="zeroinput--t"></a>zeroInput: 'T

De invoer die moet worden opgegeven `zeroOp` als `result == Zero` .


### <a name="oneop--u--unit--is-ctl"></a>oneOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

De instelbaar bewerking die moet worden toegepast wanneer `result == One` .


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