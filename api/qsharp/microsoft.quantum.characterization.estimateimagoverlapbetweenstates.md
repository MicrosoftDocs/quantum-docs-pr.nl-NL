---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Bewerking EstimateImagOverlapBetweenStates
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: f18ce43f9e5ebada4c5cc0aeff1538ac640c7390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851872"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a>Bewerking EstimateImagOverlapBetweenStates

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van twee bewerkingen die elk een kopie van een staat voorbereiden, wordt het imaginaire deel van de overlap ping tussen de staten die door elke bewerking zijn voor bereid.

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="commonpreparation--qubit--unit--is-adj"></a>commonPreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

Een bewerking waarbij een vaste invoer status wordt voor bereid.


### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt gebruik van de Hadamard-test om het imaginaire deel van $ $ \begin{align} \braket{\psi | te vinden. V ^ {\dagger} U | \psi} \end{align} $ $ waarbij $ \ket{\psi} $ de status is die is voor bereid door `commonPreparation` , $U $ is de unitary weer gave van de actie van en `preparation1` waar $V $ overeenkomt met `preparation2` .

## <a name="references"></a>Verwijzingen

- Aharonov *et al.* [quantity-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. karakte Rise ring. EstimateRealOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Micro soft. Quantum. karakte Rise ring. EstimateOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)