---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: De functie RotationPhasesAsReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 6e601cfd867b449d628da7cd60dfacd465e48860
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191190"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="cf62f-102">De functie RotationPhasesAsReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="cf62f-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="cf62f-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="cf62f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="cf62f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cf62f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cf62f-105">Hiermee worden fasen die zijn opgegeven als Qubit rotaties geconverteerd naar fasen die zijn opgegeven als gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="cf62f-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="cf62f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cf62f-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="cf62f-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="cf62f-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="cf62f-108">Matrix van rotaties met één Qubit die moeten worden geconverteerd naar gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="cf62f-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="cf62f-109">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="cf62f-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="cf62f-110">Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="cf62f-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="cf62f-111">Referenties</span><span class="sxs-lookup"><span data-stu-id="cf62f-111">References</span></span>

<span data-ttu-id="cf62f-112">We gebruiken de Conventie in</span><span class="sxs-lookup"><span data-stu-id="cf62f-112">We use the convention in</span></span>

- <span data-ttu-id="cf62f-113">[ *G.H. laag, I. L. Chuang*](https://arxiv.org/abs/1707.05391) voor de andere rotatie fasen met één Qubit om de fasen van de operator te reflecties.</span><span class="sxs-lookup"><span data-stu-id="cf62f-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>