---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Bewerking EstimateTermExpectation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 3f0ff5037b1424abb6fb318bd49ffd89f545822d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224646"
---
# <a name="estimatetermexpectation-operation"></a>Bewerking EstimateTermExpectation

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Hiermee wordt de energie berekend die is gekoppeld aan een bepaalde Jordan-Wigner Hamiltonian-term

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de verwachte waarde voor elke meet operator geschat en wordt deze vermenigvuldigd met de overeenkomstige coëfficiënt, met behulp van steek proeven.
De resultaten worden geaggregeerd in een variabele die de energie van de Jordan-Wigner term bevat.

## <a name="input"></a>Invoer

### <a name="inputstateunitary--qubit--unit--is-adj"></a>inputStateUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De unitary die wordt gebruikt voor het voorbereiden van de status.


### <a name="ops--pauli"></a>Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

De meet operatoren van de Jordan-Wigner term.


### <a name="coeffs--double"></a>coeffs: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

De coëfficiënten van de Jordan-Wigner term.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.


### <a name="nsamples--int"></a>nSamples: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachting van de term.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

De energie die is gekoppeld aan de Jordan-Wigner term.