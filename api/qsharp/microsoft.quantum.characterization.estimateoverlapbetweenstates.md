---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Bewerking EstimateOverlapBetweenStates
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 07693ccf4b8e7bbde189674d9e6b2bf7f92222f6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204297"
---
# <a name="estimateoverlapbetweenstates-operation"></a>Bewerking EstimateOverlapBetweenStates

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van twee bewerkingen waarbij elke bewerking een kopie van een staat voorbereidt, wordt een schatting gemaakt van de gekwadrateerde overlap ping tussen de staten die zijn voor bereid.

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="preparation1--qubit--unit--is-adj"></a>preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="preparation2--qubit--unit--is-adj"></a>preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

Met deze bewerking wordt de SWAP test gebruikt voor het zoeken naar $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $ waarbij $U $ de unitary weer gave van de actie van is `preparation1` en waarbij $V $ overeenkomt met `preparation2` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. karakte Rise ring. EstimateRealOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Micro soft. Quantum. karakte Rise ring. EstimateImagOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)