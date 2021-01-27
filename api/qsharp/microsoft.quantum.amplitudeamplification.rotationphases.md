---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Door de gebruiker gedefinieerd RotationPhases-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843970"
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