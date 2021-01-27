---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Bewerking ApplySequentialClassifier
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: 8186bc57e64a52e123bef8e3556d3385c4df7034
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851442"
---
# <a name="applysequentialclassifier-operation"></a><span data-ttu-id="03810-102">Bewerking ApplySequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="03810-102">ApplySequentialClassifier operation</span></span>

<span data-ttu-id="03810-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="03810-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="03810-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="03810-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="03810-105">Op basis van de structuur en het parameterisering van een sequentiële classificatie wordt de classificatie toegepast op een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="03810-105">Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.</span></span>

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="03810-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="03810-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="03810-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="03810-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="03810-108">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="03810-108">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="03810-109">Een doel registratie waarop de classificatie moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="03810-109">A target register to which the classifier should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03810-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03810-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

