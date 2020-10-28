---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Bewerking EstimateFrequency
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 83589637a7bfa328812207271844411f57d42097
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703659"
---
# <a name="estimatefrequency-operation"></a>Bewerking EstimateFrequency

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket [](https://nuget.org/packages/)


Op basis van een voor bereiding en meting, schat de frequentie waarmee deze meting slaagt (retourneert `Zero` ) door een bepaald aantal experimenten uit te voeren.

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="preparation--qubit--unit"></a>voor bereiding: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking $P $ die een bepaalde status $ \rho $ voorbereidt op de invoer register.


### <a name="measurement--qubit--__invalidresult__"></a>meting: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ongeldig <Result>__ 

Een bewerking $M $ die de afmeting van de interesse vertegenwoordigt.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarop de voor bereiding en meting elke handeling uitvoeren.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat de meting moet worden uitgevoerd om de frequentie van de interesse te schatten.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een schatting $ \hat{p} $ van de frequentie waarmee $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retourneert `Zero` , verkregen met behulp van de niet-verwerkte binomiale Estimator $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{measurements}} $, waarbij $n \_ {\uparrow} $ het aantal `Zero` waargenomen resultaten is.

Dit is met name belang rijk voor doel computers die fysieke beperkingen eerbiedigen, zodat er waarschijnlijk niet kan worden gemeten.