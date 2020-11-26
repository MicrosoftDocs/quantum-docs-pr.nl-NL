---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Bewerking MeasureWithScratch
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: c42316a811e0e4a81c7f244c093a2be88fe5c733
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227060"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="108f9-102">Bewerking MeasureWithScratch</span><span class="sxs-lookup"><span data-stu-id="108f9-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="108f9-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="108f9-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="108f9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="108f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="108f9-105">Meet de opgegeven Pauli-operator met behulp van een expliciete Scratch Qubit om de meting uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="108f9-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="108f9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="108f9-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="108f9-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="108f9-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="108f9-108">Een multi-Qubit Pauli-operator die is opgegeven als een matrix van Pauli Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="108f9-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="108f9-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="108f9-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="108f9-110">Het Qubit-REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="108f9-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="108f9-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="108f9-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="108f9-112">Het resultaat van het meten van de opgegeven Pauli-operator in het `target` REGI ster.</span><span class="sxs-lookup"><span data-stu-id="108f9-112">The result of measuring the given Pauli operator on the `target` register.</span></span>