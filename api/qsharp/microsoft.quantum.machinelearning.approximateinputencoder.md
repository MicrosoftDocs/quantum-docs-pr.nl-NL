---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: De functie ApproximateInputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 035c353c34362aa3486a7df9e7bb1bc95a6f63be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856167"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="53d95-102">De functie ApproximateInputEncoder</span><span class="sxs-lookup"><span data-stu-id="53d95-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="53d95-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="53d95-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="53d95-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="53d95-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="53d95-105">Op basis van een set coëfficiënten en een tolerantie, wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de overeenkomstige amplitude van een reken kundige status, tot aan de opgegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="53d95-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="53d95-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="53d95-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="53d95-107">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53d95-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53d95-108">De aanpassings tolerantie die moet worden gebruikt bij het coderen van de gegeven coëfficiënten in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="53d95-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="53d95-109">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="53d95-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="53d95-110">De coëfficiënten die moeten worden gecodeerd in een invoer status.</span><span class="sxs-lookup"><span data-stu-id="53d95-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="53d95-111">Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="53d95-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="53d95-112">Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="53d95-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>