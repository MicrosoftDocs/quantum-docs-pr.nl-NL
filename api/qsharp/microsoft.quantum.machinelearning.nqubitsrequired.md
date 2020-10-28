---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: De functie NQubitsRequired
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: d7ed687e9c75ed7cc71917aa1cdf32a6fbb93106
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708467"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="1d925-102">De functie NQubitsRequired</span><span class="sxs-lookup"><span data-stu-id="1d925-102">NQubitsRequired function</span></span>

<span data-ttu-id="1d925-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1d925-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="1d925-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1d925-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1d925-105">Retourneert het aantal qubits dat vereist is om een bepaalde sequentiële classificatie toe te passen.</span><span class="sxs-lookup"><span data-stu-id="1d925-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="1d925-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1d925-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="1d925-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="1d925-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="1d925-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1d925-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1d925-109">De minimale grootte van een REGI ster waarop de sequentiële classificatie kan worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1d925-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>