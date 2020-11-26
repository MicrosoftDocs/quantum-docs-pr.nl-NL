---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Door de gebruiker gedefinieerd SequentialModel-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196171"
---
# <a name="sequentialmodel-user-defined-type"></a>Door de gebruiker gedefinieerd SequentialModel-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Beschrijft een Quantum classificatie model dat bestaat uit een reeks geparametriseerde en beheerde rotaties, een toewijzing van rotatie hoeken en een afwijking tussen de twee klassen die door het model worden herkend.

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a>Benoemde items

### <a name="structure--controlledrotation"></a>Structuur: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

De volg orde van de beheerde rotaties die worden gebruikt voor het classificeren van invoer.
### <a name="parameters--double"></a>Para meters: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een toewijzing van rotatie hoeken aan de opgegeven classificatie structuur.
### <a name="bias--double"></a>Afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)

De afwijking tussen de twee klassen die door deze classificatie worden herkend.

## <a name="references"></a>Referenties

- [arXiv:1804.00633](https://arxiv.org/abs/1804.00633)