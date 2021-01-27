---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Bewerking AssertQubitWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853435"
---
# <a name="assertqubitwithintolerance-operation"></a>Bewerking AssertQubitWithinTolerance

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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