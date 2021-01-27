---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Bewerking ApplyIfZeroC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: 3876e2baf1b3ad5bbfa0097d468b1e88adf05db4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841722"
---
# <a name="applyifzeroc-operation"></a>Bewerking ApplyIfZeroC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een instelbaar bewerking toe die is voor bereid op een klassieke resultaat waarde is nul.

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a>Beschrijving

`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` . Als `One` , gebeurt er niets met `target` .
Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.

## <a name="input"></a>Invoer

### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Een meet resultaat dat bepaalt of op wordt toegepast of niet.


### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een bewerking die voorwaardelijk moet worden toegepast.


### <a name="target--t"></a>doel: 'T

De invoer waarop de bewerking wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyIfZeroC](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [Micro soft. Quantum. Canon. ApplyIfZeroA](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [Micro soft. Quantum. Canon. ApplyIfZeroCA](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)