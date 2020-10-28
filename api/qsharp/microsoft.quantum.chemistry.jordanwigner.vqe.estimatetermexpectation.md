---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Bewerking EstimateTermExpectation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703077"
---
# <a name="estimatetermexpectation-operation"></a>Bewerking EstimateTermExpectation

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket [](https://nuget.org/packages/)


Hiermee wordt de energie berekend die is gekoppeld aan een bepaalde Jordan-Wigner Hamiltonian-term

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de verwachte waarde voor elke meet operator geschat en wordt deze vermenigvuldigd met de overeenkomstige coëfficiënt, met behulp van steek proeven.
De resultaten worden geaggregeerd in een variabele die de energie van de Jordan-Wigner term bevat.

## <a name="input"></a>Invoer

### <a name="inputstateunitary--qubit--unit-adj"></a>inputStateUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

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