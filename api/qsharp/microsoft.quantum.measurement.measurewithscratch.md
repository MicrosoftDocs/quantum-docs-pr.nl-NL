---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Bewerking MeasureWithScratch
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 1ee25dbccd5bddde406cf8ed84dff77d96d7804e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706748"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="8aa8b-102">Bewerking MeasureWithScratch</span><span class="sxs-lookup"><span data-stu-id="8aa8b-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="8aa8b-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="8aa8b-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="8aa8b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8aa8b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8aa8b-105">Meet de opgegeven Pauli-operator met behulp van een expliciete Scratch Qubit om de meting uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8aa8b-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="8aa8b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8aa8b-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="8aa8b-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="8aa8b-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="8aa8b-108">Een multi-Qubit Pauli-operator die is opgegeven als een matrix van Pauli Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="8aa8b-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8aa8b-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8aa8b-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8aa8b-110">Het Qubit-REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="8aa8b-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="8aa8b-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8aa8b-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="8aa8b-112">Het resultaat van het meten van de opgegeven Pauli-operator in het `target` REGI ster.</span><span class="sxs-lookup"><span data-stu-id="8aa8b-112">The result of measuring the given Pauli operator on the `target` register.</span></span>