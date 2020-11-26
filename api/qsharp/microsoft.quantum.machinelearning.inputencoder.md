---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: De functie InputEncoder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 019161c0ef6cdec6875518ab58c8159b0f142149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211743"
---
# <a name="inputencoder-function"></a><span data-ttu-id="a9fab-102">De functie InputEncoder</span><span class="sxs-lookup"><span data-stu-id="a9fab-102">InputEncoder function</span></span>

<span data-ttu-id="a9fab-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a9fab-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a9fab-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a9fab-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a9fab-105">Op basis van een set coëfficiënten en een tolerantie wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de bijbehorende amplitude van een reken kundige status.</span><span class="sxs-lookup"><span data-stu-id="a9fab-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="a9fab-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a9fab-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a9fab-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a9fab-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a9fab-108">De coëfficiënten die moeten worden gecodeerd in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="a9fab-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="a9fab-109">Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="a9fab-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="a9fab-110">Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="a9fab-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>