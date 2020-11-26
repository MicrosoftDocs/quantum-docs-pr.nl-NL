---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: De functie CombinedStructure
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: 0a7d66be8b45d6a9df95b425e66b9b6bba241136
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211964"
---
# <a name="combinedstructure-function"></a>De functie CombinedStructure

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Als er een of meer lagen van beheerde rotaties zijn, wordt er een enkele laag met de index van de model parameter geretourneerd, zodat de afzonderlijke lagen door afzonderlijke model parameters worden para meters.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Invoer

### <a name="layers--controlledrotation"></a>lagen: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

De lagen die moeten worden gecombineerd.



## <a name="output--controlledrotation"></a>Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Een enkele laag van beheerde rotaties die de samen voeging van alle andere lagen vertegenwoordigen.