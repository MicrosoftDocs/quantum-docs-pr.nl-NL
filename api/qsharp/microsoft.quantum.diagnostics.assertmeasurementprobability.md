---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Bewerking AssertMeasurementProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830826"
---
# <a name="assertmeasurementprobability-operation"></a>Bewerking AssertMeasurementProbability

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bevestigingen die de opgegeven qubits in het gegeven Pauli meten, hebben het gegeven resultaat met de opgegeven kans, binnen een bepaalde tolerantie.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="bases--pauli"></a>basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een registratie voor het maken van de bevestiging.


### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Een verwacht resultaat van `Measure(bases, qubits)` .


### <a name="prob--double"></a>Probe: [Double](xref:microsoft.quantum.lang-ref.double)

De kans dat het gegeven resultaat wordt verwacht.


### <a name="msg--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.


### <a name="tol--double"></a>tol: [dubbel](xref:microsoft.quantum.lang-ref.double)





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertMeasurement](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)