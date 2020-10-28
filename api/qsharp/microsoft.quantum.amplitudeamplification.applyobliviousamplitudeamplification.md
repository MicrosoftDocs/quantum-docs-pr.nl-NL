---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Bewerking ApplyObliviousAmplitudeAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: a1bda344b1097c7ab3240bc6d9cd0d8df80b9662
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707741"
---
# <a name="applyobliviousamplitudeamplification-operation"></a>Bewerking ApplyObliviousAmplitudeAmplification

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Oblivious-amplitude versterking door gedeeltelijke reflecties op te geven.

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="phases--reflectionphases"></a>fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fasen van gedeeltelijke reflecties


### <a name="startstatereflection--reflectionoracle"></a>startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflectie operator over de begin status van de hulp registratie


### <a name="targetstatereflection--reflectionoracle"></a>targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflectie operator over de doel status van de hulp registratie


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Unitary Oracle $O $ van `ObliviousOracle` het type dat gezamenlijk op de hulp-en systeem registers reageert.


### <a name="auxiliaryregister--qubit"></a>auxiliaryRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Hulp registratie


### <a name="systemregister--qubit"></a>systemRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Systeem register



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Op basis van een bepaalde hulp begin status $ \ket{\Text{start}} \_ a $, een bepaalde hulp doel status $ \ket{\Text{target}} \_ a $ en een systeem status $ \ket{\psi} \_ s $, stel dat \begin{align} O\ket {\ text {start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\Text{target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\Text{target} ^ \perp} a\cdots \end{align} \_ voor sommige unitary $U $.
Met een opeenvolging van reflecties over de begin-en doel status van de hulp registratie die door toepassingen van `signalOracle` en haar adjoint wordt toegepast, kan de kans op voltooiing van het Toep assen van U worden gewijzigd.

In de meeste gevallen `auxiliaryRegister` wordt geïnitialiseerd in de status $ \ket{\Text{start}} \_ a $.

## <a name="references"></a>Naslaginformatie

Raadpleeg

- [ *D.W. Berry, A.M. Childs, r. Cleve, R. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) voor de standaard versie.
  Raadpleeg
- [ *G.H. laag, I.L. Chuang*](https://arxiv.org/abs/1610.06546) voor een generalisatie tot gedeeltelijke reflecties.