---
uid: Microsoft.Quantum.Canon.DelayedCA
title: De functie DelayedCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 8ee55e2ca7ec2cff9618b5dc66e19d88779d39ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704197"
---
# <a name="delayedca-function"></a>De functie DelayedCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit-ctl--adj"></a>op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie

Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking `op` wordt toegepast.



## <a name="output--unit--unit-ctl--adj"></a>Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit) CTL + correctie

Een nieuwe bewerking die van toepassing is op `op` invoer `arg`

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. delayed](xref:Microsoft.Quantum.Canon.Delayed)
- [Micro soft. Quantum. Canon. delay](xref:Microsoft.Quantum.Canon.Delay)