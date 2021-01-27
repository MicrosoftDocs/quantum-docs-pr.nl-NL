---
uid: Microsoft.Quantum.Canon.Delayed
title: Vertraagde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 40fcc7d0a178fdb18437b4d6c96542db593347b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840587"
---
# <a name="delayed-function"></a>Vertraagde functie

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a>Invoer

### <a name="op--t--u"></a>op: 'T> ' U 

Een bewerking die moet worden toegepast.


### <a name="arg--t"></a>arg: 'T

De invoer waarop de bewerking wordt toegepast.



## <a name="output--unit--u"></a>Output: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U 

Een nieuwe bewerking die van toepassing is op `op` invoer `arg`

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden uitgesteld.
### <a name="u"></a>' U

Het retour type van de bewerking die moet worden uitgesteld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. DelayedC](xref:Microsoft.Quantum.Canon.DelayedC)
- [Micro soft. Quantum. Canon. Delaya](xref:Microsoft.Quantum.Canon.DelayedA)
- [Micro soft. Quantum. Canon. DelayedCA](xref:Microsoft.Quantum.Canon.DelayedCA)
- [Micro soft. Quantum. Canon. delay](xref:Microsoft.Quantum.Canon.Delay)