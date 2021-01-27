---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: De functie MeasurementOperators
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835403"
---
# <a name="measurementoperators-function"></a>De functie MeasurementOperators

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


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