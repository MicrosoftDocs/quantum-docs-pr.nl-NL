---
uid: Microsoft.Quantum.Canon.DelayedC
title: De functie DelayedC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: a1f2582668131816b774bf4a8b7476d9f1ee8cad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840565"
---
# <a name="delayedc-function"></a>De functie DelayedC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking `op` wordt toegepast.



## <a name="output--unit--unit--is-ctl"></a>Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking die van toepassing is op `op` invoer `arg`

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. delayed](xref:Microsoft.Quantum.Canon.Delayed)
- [Micro soft. Quantum. Canon. delay](xref:Microsoft.Quantum.Canon.Delay)