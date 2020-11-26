---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Door de gebruiker gedefinieerd RotationPhases-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191360"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="57751-102">Door de gebruiker gedefinieerd RotationPhases-type</span><span class="sxs-lookup"><span data-stu-id="57751-102">RotationPhases user defined type</span></span>

<span data-ttu-id="57751-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="57751-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="57751-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="57751-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="57751-105">Fasen voor een opeenvolging van single-Qubit rotaties in amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="57751-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="57751-106">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="57751-106">Remarks</span></span>

<span data-ttu-id="57751-107">De eerste para meter is een reeks fasen voor reflecties, uitgedrukt als een product van Qubit draaiingen.</span><span class="sxs-lookup"><span data-stu-id="57751-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="57751-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="57751-108">[ G.H.</span></span> <span data-ttu-id="57751-109">Laag, I. L.</span><span class="sxs-lookup"><span data-stu-id="57751-109">Low, I. L.</span></span> <span data-ttu-id="57751-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="57751-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>