---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Bewerking AssertQubit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702741"
---
# <a name="assertqubit-operation"></a>Bewerking AssertQubit

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt.

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="expected--__invalidresult__"></a>verwacht: __ongeldig <Result>__

In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .


### <a name="q--qubit"></a>v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De Qubit waarvan de status wordt bevestigd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)