---
uid: Microsoft.Quantum.Preparation.ApproximatelyUnprepareArbitraryStatePlan
title: De functie ApproximatelyUnprepareArbitraryStatePlan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: d506e3a8bff365f1c99d4ed1eb41d29ba3dbeb18
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842442"
---
# <a name="approximatelyunpreparearbitrarystateplan-function"></a>De functie ApproximatelyUnprepareArbitraryStatePlan

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementatie stap van de procedure voor het voorbereiden van een wille keurige status.

```qsharp
function ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)




### <a name="coefficients--complexpolar"></a>coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="rngcontrol--range"></a>rngControl: [bereik](xref:microsoft.quantum.lang-ref.range)




### <a name="idxtarget--int"></a>idxTarget: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--qubit--unit--is-adj--ctl"></a>Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PrepareArbitraryState](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [Micro soft. Quantum. Canon. MultiplexPauli](xref:Microsoft.Quantum.Canon.MultiplexPauli)