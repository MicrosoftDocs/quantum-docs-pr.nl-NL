---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: De functie NQubitsRequired
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: e910edb9bf432e6acb5c349ee6b9d65797aaaba7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211658"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="7e103-102">De functie NQubitsRequired</span><span class="sxs-lookup"><span data-stu-id="7e103-102">NQubitsRequired function</span></span>

<span data-ttu-id="7e103-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7e103-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="7e103-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7e103-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="7e103-105">Retourneert het aantal qubits dat vereist is om een bepaalde sequentiële classificatie toe te passen.</span><span class="sxs-lookup"><span data-stu-id="7e103-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="7e103-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7e103-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="7e103-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="7e103-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="7e103-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7e103-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7e103-109">De minimale grootte van een REGI ster waarop de sequentiële classificatie kan worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="7e103-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>