---
uid: Microsoft.Quantum.Canon.Delay
title: Vertragings bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4f45527faa49f79fccff3892e928fed09f9f0bc8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216503"
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