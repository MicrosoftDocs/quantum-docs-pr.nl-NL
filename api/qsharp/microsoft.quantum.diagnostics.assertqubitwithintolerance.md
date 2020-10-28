---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Bewerking AssertQubitWithinTolerance
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702716"
---
# <a name="assertqubitwithintolerance-operation"></a>Bewerking AssertQubitWithinTolerance

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt, tot een gegeven tolerantie.

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Invoer

### <a name="expected--__invalidresult__"></a>verwacht: __ongeldig <Result>__

In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .


### <a name="q--qubit"></a>v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De Qubit waarvan de status wordt bevestigd.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Tolerantie voor de kans op een meting van de Qubit die het verwachte resultaat retourneert.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)