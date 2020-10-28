---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Bewerking MeasurePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706757"
---
# <a name="measurepaulis-operation"></a>Bewerking MeasurePaulis

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket [](https://nuget.org/packages/)


Gezien een matrix met multi-Qubit Pauli-Opera Tors, meet elk met een opgegeven meet gadget en retourneert vervolgens de matrix met resultaten.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Matrix van multi-Qubit Pauli-Opera tors die moeten worden gemeten.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Meld u aan om de gegeven Opera tors te meten.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__ 

Bewerking die de meting van een gegeven multi-Qubit-operator uitvoert.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__ []

De matrix met resultaten die zijn verkregen van het meten van elk element van `paulis` op `target` .