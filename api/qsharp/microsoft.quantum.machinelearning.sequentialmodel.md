---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Door de gebruiker gedefinieerd SequentialModel-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: ab9c121884e489b5d056285008c91c1ad70bb053
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854900"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="40451-102">Door de gebruiker gedefinieerd SequentialModel-type</span><span class="sxs-lookup"><span data-stu-id="40451-102">SequentialModel user defined type</span></span>

<span data-ttu-id="40451-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="40451-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="40451-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="40451-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="40451-105">Beschrijft een Quantum classificatie model dat bestaat uit een reeks geparametriseerde en beheerde rotaties, een toewijzing van rotatie hoeken en een afwijking tussen de twee klassen die door het model worden herkend.</span><span class="sxs-lookup"><span data-stu-id="40451-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="40451-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="40451-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="40451-107">Structuur: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="40451-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="40451-108">De volg orde van de beheerde rotaties die worden gebruikt voor het classificeren van invoer.</span><span class="sxs-lookup"><span data-stu-id="40451-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="40451-109">Para meters: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="40451-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="40451-110">Een toewijzing van rotatie hoeken aan de opgegeven classificatie structuur.</span><span class="sxs-lookup"><span data-stu-id="40451-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="40451-111">Afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="40451-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="40451-112">De afwijking tussen de twee klassen die door deze classificatie worden herkend.</span><span class="sxs-lookup"><span data-stu-id="40451-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="40451-113">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="40451-113">References</span></span>

- [<span data-ttu-id="40451-114">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="40451-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)