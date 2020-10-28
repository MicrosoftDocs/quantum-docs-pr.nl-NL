---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: De functie StandardAmplitudeAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 18228d45c4df280b004c595a7b0f1e2a607b8b2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707686"
---
# <a name="standardamplitudeamplification-function"></a>De functie StandardAmplitudeAmplification

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Standaard amplitude versterking-algoritme

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="niterations--int"></a>nIterations: [int](xref:microsoft.quantum.lang-ref.int)

Aantal iteraties $n $ van amplitude versterking


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Unitary Oracle $A $ waarmee begin status wordt voor bereid


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Index om Qubit te markeren



## <a name="output--qubit--unit-adj--ctl"></a>Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een bewerking die de standaard amplitude-versterkte Quantum algoritme implementeert

## <a name="remarks"></a>Opmerkingen

Dit is het standaard algoritme voor amplitude versterking dat wordt verkregen door de keuze van de reflectie fasen die worden berekend door de vraag `AmpAmpPhasesStandard` dat \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \End{align} deze bewerking wordt voor bereid op de status \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ text {target}} \_ s + \cdots\ket {0} \_ f \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` wordt geïnitialiseerd in de status $ \ket {0} \_ f\ket {0} \_ a $.

## <a name="references"></a>Naslaginformatie

- [*G. Brassard, P. Hoyer, M. Mosca, A. Tapp*](https://arxiv.org/abs/quant-ph/0005055)