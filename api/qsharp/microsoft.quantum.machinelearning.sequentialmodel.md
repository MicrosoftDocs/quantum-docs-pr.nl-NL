---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Door de gebruiker gedefinieerd SequentialModel-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: a425d2155489384ca81ef1c00a5e842bcfb40ae7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707962"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="14c8e-102">Door de gebruiker gedefinieerd SequentialModel-type</span><span class="sxs-lookup"><span data-stu-id="14c8e-102">SequentialModel user defined type</span></span>

<span data-ttu-id="14c8e-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="14c8e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="14c8e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="14c8e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="14c8e-105">Beschrijft een Quantum classificatie model dat bestaat uit een reeks geparametriseerde en beheerde rotaties, een toewijzing van rotatie hoeken en een afwijking tussen de twee klassen die door het model worden herkend.</span><span class="sxs-lookup"><span data-stu-id="14c8e-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="14c8e-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="14c8e-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="14c8e-107">Structuur: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="14c8e-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="14c8e-108">De volg orde van de beheerde rotaties die worden gebruikt voor het classificeren van invoer.</span><span class="sxs-lookup"><span data-stu-id="14c8e-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="14c8e-109">Para meters: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="14c8e-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="14c8e-110">Een toewijzing van rotatie hoeken aan de opgegeven classificatie structuur.</span><span class="sxs-lookup"><span data-stu-id="14c8e-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="14c8e-111">Afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="14c8e-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="14c8e-112">De afwijking tussen de twee klassen die door deze classificatie worden herkend.</span><span class="sxs-lookup"><span data-stu-id="14c8e-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="14c8e-113">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="14c8e-113">References</span></span>

- [<span data-ttu-id="14c8e-114">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="14c8e-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)