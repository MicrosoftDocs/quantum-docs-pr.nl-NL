---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Bewerking AssertProbInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707437"
---
# <a name="assertprobint-operation"></a>Bewerking AssertProbInt

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Hiermee wordt bevestigd dat de kans op een specifieke status van een Quantum register de verwachte waarde heeft.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>Beschrijving

Gezien een $n $-Qubit Quantum State $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, bevestigt u dat de kans $ | \ alpha_j | ^ 2 $ van de status $ \ket{j} $ geïndexeerd door $j $ de verwachte waarde heeft.

## <a name="input"></a>Invoer

### <a name="stateindex--int"></a>stateIndex: [int](xref:microsoft.quantum.lang-ref.int)

De index $j $ van de status $ \ket{j} $ vertegenwoordigd door een `LittleEndian` REGI ster.


### <a name="expected--double"></a>verwacht: [Double](xref:microsoft.quantum.lang-ref.double)

De verwachte waarde van $ | \ alpha_j | ^ 2 $.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het Qubit-REGI ster waarin $ \ket{\psi} $ wordt opgeslagen in de indeling little-endian.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Absolute tolerantie voor het verschil tussen werkelijk en verwacht.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

