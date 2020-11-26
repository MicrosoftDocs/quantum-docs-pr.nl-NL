---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Bewerking ApplyAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: 0b40f94633bb43df5e64cd16d5ac8e12bcd1cc4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191564"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="4a9c4-102">Bewerking ApplyAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="4a9c4-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="4a9c4-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4a9c4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a9c4-105">Hiermee past u de amplitude versterking op een bepaald REGI ster toe met behulp van een bepaalde reeks fasen en Oracle-waarden die betrekking hebben op de initiële en de laatste status.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4a9c4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4a9c4-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="4a9c4-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="4a9c4-108">Een reeks fasen waarin de gedeeltelijke reflecties in elke stap van de amplitude versterking algoritme worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="4a9c4-109">Zie @"microsoft.quantum.amplitudeamplification.standardreflectionphases" voor een voor beeld.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="4a9c4-110">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="4a9c4-111">Een Oracle die de oorspronkelijke status weerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="4a9c4-112">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="4a9c4-113">Een Oracle die de gewenste eind status weergeeft.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="4a9c4-114">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4a9c4-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4a9c4-115">Een REGI ster voor het uitvoeren van amplitude versterking op.</span><span class="sxs-lookup"><span data-stu-id="4a9c4-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4a9c4-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a9c4-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

