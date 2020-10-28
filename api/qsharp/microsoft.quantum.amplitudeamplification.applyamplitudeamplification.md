---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Bewerking ApplyAmplitudeAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: be884eab70c7f72f994baf6bd7caf05769e0d5f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707764"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="bdd57-102">Bewerking ApplyAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="bdd57-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="bdd57-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="bdd57-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="bdd57-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bdd57-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bdd57-105">Hiermee past u de amplitude versterking op een bepaald REGI ster toe met behulp van een bepaalde reeks fasen en Oracle-waarden die betrekking hebben op de initiële en de laatste status.</span><span class="sxs-lookup"><span data-stu-id="bdd57-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="bdd57-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bdd57-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="bdd57-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="bdd57-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="bdd57-108">Een reeks fasen waarin de gedeeltelijke reflecties in elke stap van de amplitude versterking algoritme worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="bdd57-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="bdd57-109">Zie @"microsoft.quantum.amplitudeamplification.standardreflectionphases" voor een voor beeld.</span><span class="sxs-lookup"><span data-stu-id="bdd57-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="bdd57-110">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="bdd57-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="bdd57-111">Een Oracle die de oorspronkelijke status weerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="bdd57-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="bdd57-112">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="bdd57-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="bdd57-113">Een Oracle die de gewenste eind status weergeeft.</span><span class="sxs-lookup"><span data-stu-id="bdd57-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bdd57-114">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bdd57-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bdd57-115">Een REGI ster voor het uitvoeren van amplitude versterking op.</span><span class="sxs-lookup"><span data-stu-id="bdd57-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bdd57-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bdd57-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

