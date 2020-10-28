---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Bewerking EstimateRealOverlapBetweenStates
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 01631bcbff2bff26ddc1db4e42d90ac4f8380bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703611"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a>Bewerking EstimateRealOverlapBetweenStates

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket [](https://nuget.org/packages/)


Op basis van twee bewerkingen die elk een kopie van een staat voorbereiden, wordt het werkelijke deel van de overlap ping tussen de staten die door elke bewerking zijn voor bereid, geschat.

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="commonpreparation--qubit--unit-adj"></a>commonPreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Een bewerking waarbij een vaste invoer status wordt voor bereid.


### <a name="preparation1--qubit--unit-adj--ctl"></a>preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="preparation2--qubit--unit-adj--ctl"></a>preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt gebruik van de Hadamard-test om het echte deel van $ $ \begin{align} \braket{\psi te vinden. V ^ {\dagger} U | \psi} \end{align} $ $ waarbij $ \ket{\psi} $ de status is die is voor bereid door `commonPreparation` , $U $ is de unitary weer gave van de actie van en `preparation1` waar $V $ overeenkomt met `preparation2` .

## <a name="references"></a>Naslaginformatie

- Aharonov *et al.* [quantity-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. karakte Rise ring. EstimateImagOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [Micro soft. Quantum. karakte Rise ring. EstimateOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)