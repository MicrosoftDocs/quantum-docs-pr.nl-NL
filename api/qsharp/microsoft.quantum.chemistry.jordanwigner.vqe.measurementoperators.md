---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: De functie MeasurementOperators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703058"
---
# <a name="measurementoperators-function"></a>De functie MeasurementOperators

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket [](https://nuget.org/packages/)


Berekent alle meet operatoren die vereist zijn voor het berekenen van de verwachting van een Jordan-Wigner term.

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.


### <a name="indices--int"></a>indices: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix met de indices van de Qubit waarop elke Pauli-operator wordt toegepast.


### <a name="termtype--int"></a>termType: [int](xref:microsoft.quantum.lang-ref.int)

Het type Jordan-Wigner-term.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Een matrix met meet operatoren (elk een matrix van Pauli).