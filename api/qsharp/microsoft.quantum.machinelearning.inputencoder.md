---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: De functie InputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852943"
---
# <a name="inputencoder-function"></a><span data-ttu-id="0ec5f-102">De functie InputEncoder</span><span class="sxs-lookup"><span data-stu-id="0ec5f-102">InputEncoder function</span></span>

<span data-ttu-id="0ec5f-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="0ec5f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="0ec5f-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="0ec5f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="0ec5f-105">Op basis van een set coëfficiënten en een tolerantie wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de bijbehorende amplitude van een reken kundige status.</span><span class="sxs-lookup"><span data-stu-id="0ec5f-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="0ec5f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0ec5f-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="0ec5f-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0ec5f-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0ec5f-108">De coëfficiënten die moeten worden gecodeerd in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="0ec5f-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="0ec5f-109">Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="0ec5f-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="0ec5f-110">Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="0ec5f-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>