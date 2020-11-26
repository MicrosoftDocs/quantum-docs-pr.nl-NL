---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Bewerking EstimateFrequencyA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: f12fc150de5bcea3d53ce88003c71976d8f2467f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204348"
---
# <a name="estimatefrequencya-operation"></a>Bewerking EstimateFrequencyA

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een voor bereiding die adjointable en meting levert, wordt een schatting gemaakt van de frequentie waarmee deze meting slaagt (retourneert `Zero` ) door een bepaald aantal experimenten uit te voeren.

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="preparation--qubit--unit--is-adj"></a>voor bereiding: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

Een adjointable-bewerking $P $ die een bepaalde status $ \rho $ voorbereidt op de invoer register.


### <a name="measurement--qubit--__invalidresult__"></a>meting: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ongeldig <Result>__ 

Een bewerking $M $ die de afmeting van de interesse vertegenwoordigt.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarop de voor bereiding en meting elke handeling uitvoeren.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat de meting moet worden uitgevoerd om de frequentie van de interesse te schatten.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een schatting $ \hat{p} $ van de frequentie waarmee $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retourneert `Zero` , verkregen met behulp van de niet-verwerkte binomiale Estimator $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{measurements}} $, waarbij $n \_ {\uparrow} $ het aantal `Zero` waargenomen resultaten is.

## <a name="remarks"></a>Opmerkingen

Voor adjointable-bewerkingen kunnen bepaalde hypo Thesen worden gemaakt, zoals het aanroepen van de bewerking, wordt de qubits voor bereid op exact dezelfde staat, zodat doel machines een aantal prestatie optimalisaties mogelijk maken.