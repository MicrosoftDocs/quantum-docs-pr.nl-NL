---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Bewerking ApplyIfElseBC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 6140a8382cbd00589d1aef99e004f71f5d9295a9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841821"
---
# <a name="applyifelsebc-operation"></a>Bewerking ApplyIfElseBC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een van de twee instel bare bewerkingen toe, afhankelijk van de waarde van een klassieke bit.

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a>Beschrijving

Gezien een bit `bit` , wordt de bewerking `trueOp` met `trueInput` als invoer toegepast `bit` `true` en toegepast als dat zo `falseOp(falseInput)` is `bit` `false` .

## <a name="input"></a>Invoer

### <a name="bit--bool"></a>bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De Booleaanse waarde die wordt gebruikt om te bepalen of deze `trueOp` `falseOp` is toegepast.


### <a name="trueop--t--unit--is-ctl"></a>trueOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

De instelbaar bewerking die moet worden toegepast wanneer dat het geval `bit` is `true` .


### <a name="trueinput--t"></a>trueInput: 'T

De invoer die moet worden opgegeven `trueOp` als `bit` `true` .


### <a name="falseop--u--unit--is-ctl"></a>falseOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

De instelbaar bewerking die moet worden toegepast wanneer dat het geval `bit` is `false` .


### <a name="falseinput--u"></a>falseInput: ' U

De invoer die moet worden opgegeven `falseOp` als `bit` `false` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking `trueOp` die voorwaardelijk moet worden toegepast.
### <a name="u"></a>' U

Het invoer type van de bewerking `falseOp` die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Micro soft. Quantum. Canon. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Micro soft. Quantum. Canon. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Micro soft. Quantum. Canon. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Micro soft. Quantum. Canon. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)