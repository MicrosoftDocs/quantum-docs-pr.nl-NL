---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Door de gebruiker gedefinieerd RotationPhases-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707693"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="18782-102">Door de gebruiker gedefinieerd RotationPhases-type</span><span class="sxs-lookup"><span data-stu-id="18782-102">RotationPhases user defined type</span></span>

<span data-ttu-id="18782-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="18782-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="18782-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="18782-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="18782-105">Fasen voor een opeenvolging van single-Qubit rotaties in amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="18782-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="18782-106">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="18782-106">Remarks</span></span>

<span data-ttu-id="18782-107">De eerste para meter is een reeks fasen voor reflecties, uitgedrukt als een product van Qubit draaiingen.</span><span class="sxs-lookup"><span data-stu-id="18782-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="18782-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="18782-108">[ G.H.</span></span> <span data-ttu-id="18782-109">Laag, I. L.</span><span class="sxs-lookup"><span data-stu-id="18782-109">Low, I. L.</span></span> <span data-ttu-id="18782-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="18782-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>