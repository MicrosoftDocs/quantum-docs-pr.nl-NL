---
uid: Microsoft.Quantum.Canon.Delay
title: Vertragings bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840643"
---
# <a name="delay-operation"></a>Vertragings bewerking

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bepaalde bewerking toegepast met een vertraging.

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a>Beschrijving

Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.
Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.
Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .

## <a name="input"></a>Invoer

### <a name="op--t--u"></a>op: 'T> ' U 

Een bewerking die moet worden toegepast.


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking wordt toegepast.


### <a name="aux--unit"></a>AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)

Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.



## <a name="output--u"></a>Uitvoer: ' U



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.
### <a name="u"></a>' U

Het retour type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. DelayC](xref:Microsoft.Quantum.Canon.DelayC)
- [Micro soft. Quantum. Canon. Delaya](xref:Microsoft.Quantum.Canon.DelayA)
- [Micro soft. Quantum. Canon. DelayCA](xref:Microsoft.Quantum.Canon.DelayCA)
- [Micro soft. Quantum. Canon. delayed](xref:Microsoft.Quantum.Canon.Delayed)