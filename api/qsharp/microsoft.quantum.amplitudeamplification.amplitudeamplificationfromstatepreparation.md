---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: De functie AmplitudeAmplificationFromStatePreparation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: e64ad5ad4e975483f20f92c0b070dd6788ef296b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847444"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a>De functie AmplitudeAmplificationFromStatePreparation

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een amplitude versterking van Oracle voor gedeeltelijke reflecties.

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="phases--reflectionphases"></a>fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fasen van gedeeltelijke reflecties


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Unitary Oracle $A $ waarmee begin status wordt voor bereid


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Index om Qubit te markeren



## <a name="output--qubit--unit--is-adj--ctl"></a>Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking waarbij amplitude versterking wordt geïmplementeerd door Oracle die worden geïmplementeerd door gedeeltelijke reflecties.

## <a name="remarks"></a>Opmerkingen

Dit legt strengere voor waarden vast in de vorm van de begin-en doel status dan in `AmpAmpByReflectionPhases` .
Er wordt van uitgegaan dat de doel status is gemarkeerd met $ \ket {1} \_ f $.
Er wordt van uitgegaan dat \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` worden geïnitialiseerd met de status $ \ket {0} \_ {f} \ket {0} \_ s $.