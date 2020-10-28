---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: De functie InputEncoder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 771cf01866498f4662864939e6946526c2b5827a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701373"
---
# <a name="inputencoder-function"></a><span data-ttu-id="b9818-102">De functie InputEncoder</span><span class="sxs-lookup"><span data-stu-id="b9818-102">InputEncoder function</span></span>

<span data-ttu-id="b9818-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b9818-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b9818-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b9818-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b9818-105">Op basis van een set coëfficiënten en een tolerantie wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de bijbehorende amplitude van een reken kundige status.</span><span class="sxs-lookup"><span data-stu-id="b9818-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="b9818-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b9818-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="b9818-107">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b9818-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b9818-108">De coëfficiënten die moeten worden gecodeerd in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="b9818-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="b9818-109">Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="b9818-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="b9818-110">Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="b9818-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>