---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: De functie ApproximateInputEncoder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706885"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="2333b-102">De functie ApproximateInputEncoder</span><span class="sxs-lookup"><span data-stu-id="2333b-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="2333b-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2333b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2333b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2333b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2333b-105">Op basis van een set coëfficiënten en een tolerantie, wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de overeenkomstige amplitude van een reken kundige status, tot aan de opgegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="2333b-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="2333b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2333b-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="2333b-107">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2333b-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2333b-108">De aanpassings tolerantie die moet worden gebruikt bij het coderen van de gegeven coëfficiënten in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="2333b-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="2333b-109">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2333b-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2333b-110">De coëfficiënten die moeten worden gecodeerd in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="2333b-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="2333b-111">Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="2333b-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="2333b-112">Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="2333b-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>