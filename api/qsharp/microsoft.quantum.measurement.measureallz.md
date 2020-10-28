---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Bewerking MeasureAllZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701942"
---
# <a name="measureallz-operation"></a>Bewerking MeasureAllZ

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket [](https://nuget.org/packages/)


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