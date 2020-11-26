---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Bewerking MeasurePaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194216"
---
# <a name="measurepaulis-operation"></a>Bewerking MeasurePaulis

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gezien een matrix met multi-Qubit Pauli-Opera Tors, meet elk met een opgegeven meet gadget en retourneert vervolgens de matrix met resultaten.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Matrix van multi-Qubit Pauli-Opera tors die moeten worden gemeten.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Meld u aan om de gegeven Opera tors te meten.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__ 

Bewerking die de meting van een gegeven multi-Qubit-operator uitvoert.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__[]

De matrix met resultaten die zijn verkregen van het meten van elk element van `paulis` op `target` .