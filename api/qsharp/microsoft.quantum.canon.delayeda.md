---
uid: Microsoft.Quantum.Canon.DelayedA
title: De functie delayed
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704213"
---
# <a name="delayeda-function"></a>De functie delayed

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit-adj"></a>op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking `op` wordt toegepast.



## <a name="output--unit--unit-adj"></a>Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit) correctie

Een nieuwe bewerking die van toepassing is op `op` invoer `arg`

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. delayed](xref:Microsoft.Quantum.Canon.Delayed)
- [Micro soft. Quantum. Canon. delay](xref:Microsoft.Quantum.Canon.Delay)