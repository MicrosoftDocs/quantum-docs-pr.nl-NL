---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: De functie IntsToPaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 2333dcbd2988480e2b2b9b217b26705f3578de00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230528"
---
# <a name="intstopaulis-function"></a>De functie IntsToPaulis

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converteert een matrix met gehele getallen naar een matrix van Pauli-Opera tors met één Qubit.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Invoer

### <a name="ints--int"></a>ints: [int](xref:microsoft.quantum.lang-ref.int)[]

Matrix van gehele getallen in het bereik `0..3`  dat moet worden geconverteerd naar Pauli-Opera tors.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een matrix `paulis` van Pauli-Opera tors `Pauli[]` met dezelfde lengte als `ints` die `paulis[idxPauli]` gelijk is aan het element van `[PauliI, PauliX, PauliY, PauliZ]` gegeven door `ints[idxPauli]` .