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
# <a name="combinedstructure-function"></a><span data-ttu-id="35d30-102">De functie CombinedStructure</span><span class="sxs-lookup"><span data-stu-id="35d30-102">CombinedStructure function</span></span>

<span data-ttu-id="35d30-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="35d30-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="35d30-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="35d30-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="35d30-105">Als er een of meer lagen van beheerde rotaties zijn, wordt er een enkele laag met de index van de model parameter geretourneerd, zodat de afzonderlijke lagen door afzonderlijke model parameters worden para meters.</span><span class="sxs-lookup"><span data-stu-id="35d30-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="35d30-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="35d30-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="35d30-107">lagen: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="35d30-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="35d30-108">De lagen die moeten worden gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="35d30-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="35d30-109">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="35d30-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="35d30-110">Een enkele laag van beheerde rotaties die de samen voeging van alle andere lagen vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="35d30-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>