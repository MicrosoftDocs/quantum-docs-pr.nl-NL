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
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="fbaf4-102">Door de gebruiker gedefinieerd SequentialModel-type</span><span class="sxs-lookup"><span data-stu-id="fbaf4-102">SequentialModel user defined type</span></span>

<span data-ttu-id="fbaf4-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fbaf4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="fbaf4-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fbaf4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="fbaf4-105">Beschrijft een Quantum classificatie model dat bestaat uit een reeks geparametriseerde en beheerde rotaties, een toewijzing van rotatie hoeken en een afwijking tussen de twee klassen die door het model worden herkend.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="fbaf4-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="fbaf4-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="fbaf4-107">Structuur: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="fbaf4-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="fbaf4-108">De volg orde van de beheerde rotaties die worden gebruikt voor het classificeren van invoer.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="fbaf4-109">Para meters: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="fbaf4-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="fbaf4-110">Een toewijzing van rotatie hoeken aan de opgegeven classificatie structuur.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="fbaf4-111">Afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fbaf4-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fbaf4-112">De afwijking tussen de twee klassen die door deze classificatie worden herkend.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="fbaf4-113">Referenties</span><span class="sxs-lookup"><span data-stu-id="fbaf4-113">References</span></span>

- [<span data-ttu-id="fbaf4-114">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="fbaf4-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)