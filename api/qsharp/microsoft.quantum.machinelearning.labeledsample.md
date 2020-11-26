---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Door de gebruiker gedefinieerd LabeledSample-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196324"
---
# <a name="labeledsample-user-defined-type"></a>Door de gebruiker gedefinieerd LabeledSample-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Een voor beeld, voorzien van een klasse waarvan het voor beeld deel uitmaakt.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="features--double"></a>Functies: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Een vector van functies voor het gegeven voor beeld.
### <a name="label--int"></a>Label: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal voor de klasse waarvan dit voor beeld deel uitmaakt.