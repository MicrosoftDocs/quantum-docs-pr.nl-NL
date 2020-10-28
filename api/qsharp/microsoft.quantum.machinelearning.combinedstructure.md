---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: De functie CombinedStructure
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706876"
---
# <a name="combinedstructure-function"></a>De functie CombinedStructure

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Als er een of meer lagen van beheerde rotaties zijn, wordt er een enkele laag met de index van de model parameter geretourneerd, zodat de afzonderlijke lagen door afzonderlijke model parameters worden para meters.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Invoer

### <a name="layers--controlledrotation"></a>lagen: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

De lagen die moeten worden gecombineerd.



## <a name="output--controlledrotation"></a>Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Een enkele laag van beheerde rotaties die de samen voeging van alle andere lagen vertegenwoordigen.