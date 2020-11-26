---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Door de gebruiker gedefinieerd RotationPhases-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191360"
---
# <a name="rotationphases-user-defined-type"></a>Door de gebruiker gedefinieerd RotationPhases-type

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Fasen voor een opeenvolging van single-Qubit rotaties in amplitude versterking.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Opmerkingen

De eerste para meter is een reeks fasen voor reflecties, uitgedrukt als een product van Qubit draaiingen.
[ G.H. Laag, I. L. Chuang, https://arxiv.org/abs/1707.05391 ].