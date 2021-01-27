---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Door de gebruiker gedefinieerd LabeledSample-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846967"
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