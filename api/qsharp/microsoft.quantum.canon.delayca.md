---
uid: Microsoft.Quantum.Canon.DelayCA
title: Bewerking DelayCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a8606cde976882bba0eb23467932b9ee0ed36696
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840624"
---
# <a name="delayca-operation"></a>Bewerking DelayCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bepaalde bewerking toegepast met een vertraging.

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.
Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.
Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .

## <a name="input"></a>Invoer

### <a name="op--t--unit--is-adj--ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die moet worden toegepast.


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking wordt toegepast.


### <a name="aux--unit"></a>AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)

Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. delay](xref:Microsoft.Quantum.Canon.Delay)
- [Micro soft. Quantum. Canon. delayed](xref:Microsoft.Quantum.Canon.Delayed)