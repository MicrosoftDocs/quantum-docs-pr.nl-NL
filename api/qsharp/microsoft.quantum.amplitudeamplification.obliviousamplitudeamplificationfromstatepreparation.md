---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: De functie ObliviousAmplitudeAmplificationFromStatePreparation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707722"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>De functie ObliviousAmplitudeAmplificationFromStatePreparation

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Oblivious-amplitude versterking door Oracle voor gedeeltelijke reflecties.

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="phases--reflectionphases"></a>fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fasen van gedeeltelijke reflecties


### <a name="startstateoracle--deterministicstateoracle"></a>startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Unitary Oracle $A $ waarmee de start status van de hulp wordt voor bereid


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Unitary Oracle $O $ van `ObliviousOracle` het type dat gezamenlijk op de hulp-en systeem register reageert


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Index naar één Qubit-vlag registreren



## <a name="output--qubitqubit--unit-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een bewerking die Oblivious amplitude-versterking implementeert op basis van gedeeltelijke reflecties.

## <a name="remarks"></a>Opmerkingen

Dit legt strengere voor waarden vast in de vorm van het hulp start en de doel statussen dan in `AmpAmpObliviousByReflectionPhases` .
Er wordt van uitgegaan dat $A \ket {0} \_ f\ket {0} \_ A = \ket{\Text{start}} \_ {FA} $ de hulp start status $ \ket{\Text{start}} \_ {FA} $ voorbereidt op basis van de reken kracht $ \ket {0} \_ f\ket {0} $.
Er wordt van uitgegaan dat de doel status is gemarkeerd met $ \ket {1} \_ f $.
Er wordt van uitgegaan dat \begin{align} O\ket {\ text {start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ text {overal}} \_ a\ket {\ text {target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} voor sommige unitary $U $.