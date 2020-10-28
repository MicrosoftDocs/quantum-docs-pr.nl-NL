---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Door de gebruiker gedefinieerd LabeledSample-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702051"
---
# <a name="labeledsample-user-defined-type"></a>Door de gebruiker gedefinieerd LabeledSample-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Een voor beeld, voorzien van een klasse waarvan het voor beeld deel uitmaakt.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="features--double"></a>Functies: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Een vector van functies voor het gegeven voor beeld.
### <a name="label--int"></a>Label: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal voor de klasse waarvan dit voor beeld deel uitmaakt.