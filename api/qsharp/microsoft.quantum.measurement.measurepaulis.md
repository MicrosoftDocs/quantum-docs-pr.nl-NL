---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Bewerking MeasurePaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194216"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="9faea-102">Bewerking MeasurePaulis</span><span class="sxs-lookup"><span data-stu-id="9faea-102">MeasurePaulis operation</span></span>

<span data-ttu-id="9faea-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="9faea-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="9faea-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9faea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9faea-105">Gezien een matrix met multi-Qubit Pauli-Opera Tors, meet elk met een opgegeven meet gadget en retourneert vervolgens de matrix met resultaten.</span><span class="sxs-lookup"><span data-stu-id="9faea-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="9faea-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9faea-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="9faea-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="9faea-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="9faea-108">Matrix van multi-Qubit Pauli-Opera tors die moeten worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="9faea-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9faea-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9faea-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9faea-110">Meld u aan om de gegeven Opera tors te meten.</span><span class="sxs-lookup"><span data-stu-id="9faea-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="9faea-111">Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9faea-111">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="9faea-112">Bewerking die de meting van een gegeven multi-Qubit-operator uitvoert.</span><span class="sxs-lookup"><span data-stu-id="9faea-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9faea-113">Uitvoer: __ongeldig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="9faea-113">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="9faea-114">De matrix met resultaten die zijn verkregen van het meten van elk element van `paulis` op `target` .</span><span class="sxs-lookup"><span data-stu-id="9faea-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>