---
uid: Microsoft.Quantum.Canon.DelayA
title: Vertragings bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 77c40633824ccd9250252804b08d7400936515dd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704244"
---
# <a name="delaya-operation"></a>Vertragings bewerking

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bepaalde bewerking toegepast met een vertraging.

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a>Beschrijving

Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.
Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.
Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .

## <a name="input"></a>Invoer

### <a name="op--t--unit-adj"></a>op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

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