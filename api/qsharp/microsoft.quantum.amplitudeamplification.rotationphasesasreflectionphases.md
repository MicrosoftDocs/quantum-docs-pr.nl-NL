---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: De functie RotationPhasesAsReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: d62a7584324c9467ccc759e4bed81acbceee719c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707687"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="24ace-102">De functie RotationPhasesAsReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="24ace-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="24ace-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="24ace-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="24ace-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24ace-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24ace-105">Hiermee worden fasen die zijn opgegeven als Qubit rotaties geconverteerd naar fasen die zijn opgegeven als gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="24ace-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="24ace-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="24ace-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="24ace-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="24ace-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="24ace-108">Matrix van rotaties met één Qubit die moeten worden geconverteerd naar gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="24ace-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="24ace-109">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="24ace-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="24ace-110">Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="24ace-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="24ace-111">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="24ace-111">References</span></span>

<span data-ttu-id="24ace-112">We gebruiken de Conventie in</span><span class="sxs-lookup"><span data-stu-id="24ace-112">We use the convention in</span></span>

- <span data-ttu-id="24ace-113">[ *G.H. laag, I. L. Chuang*](https://arxiv.org/abs/1707.05391) voor de andere rotatie fasen met één Qubit om de fasen van de operator te reflecties.</span><span class="sxs-lookup"><span data-stu-id="24ace-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>