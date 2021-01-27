---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Bewerking AssertProbInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843409"
---
# <a name="assertprobint-operation"></a>Bewerking AssertProbInt

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Voorbeeld

Stel dat het `qubits` REGI ster een 3-Qubit Quantum State $ \ket{\psi} = \ SQRT {1/8} \ Ket {0} + \ SQRT {7/8} \ Ket {6} $ in de indeling little endian codeert.
Dit betekent dat het aantal statussen $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ en $ \ket \equiv\ket \ket \ket {6} {0} {1} {1} $. Daarna slagen de volgende verklaringen:

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```