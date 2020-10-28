---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Door de gebruiker gedefinieerd RotationPhases-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707693"
---
# <a name="rotationphases-user-defined-type"></a>Door de gebruiker gedefinieerd RotationPhases-type

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Fasen voor een opeenvolging van single-Qubit rotaties in amplitude versterking.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Opmerkingen

De eerste para meter is een reeks fasen voor reflecties, uitgedrukt als een product van Qubit draaiingen.
[ G.H. Laag, I. L. Chuang, https://arxiv.org/abs/1707.05391 ].