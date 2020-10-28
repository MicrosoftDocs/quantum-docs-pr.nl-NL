---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: De functie RotationPhasesAsReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: d62a7584324c9467ccc759e4bed81acbceee719c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707687"
---
# <a name="rotationphasesasreflectionphases-function"></a>De functie RotationPhasesAsReflectionPhases

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Hiermee worden fasen die zijn opgegeven als Qubit rotaties geconverteerd naar fasen die zijn opgegeven als gedeeltelijke reflecties.

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Invoer

### <a name="rotphases--rotationphases"></a>rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)

Matrix van rotaties met één Qubit die moeten worden geconverteerd naar gedeeltelijke reflecties.



## <a name="output--reflectionphases"></a>Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties.

## <a name="references"></a>Naslaginformatie

We gebruiken de Conventie in

- [ *G.H. laag, I. L. Chuang*](https://arxiv.org/abs/1707.05391) voor de andere rotatie fasen met één Qubit om de fasen van de operator te reflecties.