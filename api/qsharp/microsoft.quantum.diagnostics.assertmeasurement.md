---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Bewerking AssertMeasurement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702782"
---
# <a name="assertmeasurement-operation"></a>Bewerking AssertMeasurement

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Bevestigingen die de opgegeven qubits in het opgegeven Pauli meten, zullen altijd het gegeven resultaat hebben.

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="bases--pauli"></a>basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een registratie voor het maken van de bevestiging.


### <a name="result--__invalidresult__"></a>resultaat: __ongeldig <Result>__

Het verwachte resultaat van `Measure(bases, qubits)` .


### <a name="msg--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertMeasurementProbability](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)