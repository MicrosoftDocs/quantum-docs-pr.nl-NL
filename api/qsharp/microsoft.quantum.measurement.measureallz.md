---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Bewerking MeasureAllZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227077"
---
# <a name="measureallz-operation"></a>Bewerking MeasureAllZ

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gezamenlijk meet het REGI ster van qubits in de Pauli Z-basis.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>Beschrijving

Meting van een REGI ster van qubits in de $Z \otimes Z \otimes \cdots \otimes Z $ soort_jaar, waarmee de pariteit van het volledige REGI ster wordt aangegeven.

## <a name="input"></a>Invoer

### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Het REGI ster dat moet worden gemeten.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

Het resultaat van de meting $Z \otimes Z \otimes \cdots \otimes Z $.