---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Bewerking RandomWalkPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 2c3afdd41da24a1f32f59f36f0f5c5ed29df1f0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226159"
---
# <a name="randomwalkphaseestimation-operation"></a>Bewerking RandomWalkPhaseEstimation

Naam ruimte: [micro soft. Quantum. Research. karakte Rise](xref:Microsoft.Quantum.Research.Characterization) ring

Pakket: [micro soft. Quantum. Research. karakte Rise](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization) ring


Voert een iteratieve fase schatting uit met behulp van een wille keurige Walk om Bayesiaanse te benaderen bij de klassieke meet resultaten van een bepaalde Oracle-en eigenstate.

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Invoer

### <a name="initialmean--double"></a>initialMean: [dubbel](xref:microsoft.quantum.lang-ref.double)

Gemiddelde van de aanvankelijke voorafgaande distributie over $ \phi $.


### <a name="initialstddev--double"></a>initialStdDev: [dubbel](xref:microsoft.quantum.lang-ref.double)

Standaard afwijking van de aanvankelijke voorafgaande distributie over $ \phi $.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Aantal metingen dat moet worden geaccepteerd in de uiteindelijke posterior-schatting.


### <a name="maxmeasurements--int"></a>maxMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het totale aantal metingen dat kan worden uitgevoerd voordat de bewerking als mislukt wordt beschouwd.


### <a name="unwind--int"></a>afwikkeling: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal resultaten dat moet worden verg eten wanneer consistentie controles mislukt.


### <a name="oracle--continuousoracle"></a>Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Een bewerking die een unitary $U $ zodanig vertegenwoordigt dat $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ voor eigenstates $ \ket{\phi} $ met onbekende fase $ \phi \in \mathbb{R} ^ + $.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster waarop $ wordt $U.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

De laatste schatting $ \hat{\phi} \mathrel{: =} \expect [\phi] $, waarbij de verwachting groter is dan het posterior gegeven alle geaccepteerde gegevens.

## <a name="remarks"></a>Opmerkingen

### <a name="iterative-phase-estimation-and-eigenstates"></a>Schatting van iteratieve fase en Eigenstates

Over het algemeen hoeft het invoer register `eigenstate` geen eigenstate $ \ket{\phi} $ van $U $ te zijn, maar dit kan een superpositie zijn dan eigenstates. Stel dat de invoer status wordt gegeven door \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j}, \end{align} waarbij $ \{ \alpha \_ j \} $ complexe coëfficiënten is, zoals $ \sum \_ j | \alpha \_ j | ^ 2 = $1 en waarbij $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $.

Vervolgens wordt de schatting van de iteratieve fase geconvergeerd naar één eigenstate, zoals beschreven in de [ontwikkel handleiding](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).

### <a name="experiment-design"></a>Experiment ontwerpen

De meet tijden $t $ en de inversie-hoeken $ \theta $ die zijn door gegeven aan `oracle` worden gekozen op basis van de *heuristiek* van de partikel, \Begin{align} \theta \sim \Pr (\phi), \quad t \approx \frac {1} {\variance{\phi}}.
\end{align} deze heuristiek is optimaal voor het verminderen van de verwachte posterior afwijking in een iteratieve fase schatting, onder de veronderstelling van een normaal voor gaande.

### <a name="optimality"></a>Optimale prestaties

Met deze bewerking wordt gebruikgemaakt van de optimale Estimator voor de fase $ \phi $, zoals geëvalueerd met behulp van het kwadratische verlies $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $.

Zie de schatting van de [Bayesiaanse-fase](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) voor meer informatie over de statistieken van iteratieve fase schatting.

## <a name="references"></a>Referenties

- Ferrie *et al.* 2011 [DOI: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).
- Wiebe *et al.* 2013 [DOI: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)
- Wiebe en Granade 2018 *(in voor bereiding)*.