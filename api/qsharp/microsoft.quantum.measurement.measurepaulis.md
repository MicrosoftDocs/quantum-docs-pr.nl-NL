---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Bewerking MeasurePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706757"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="1328e-102">Bewerking MeasurePaulis</span><span class="sxs-lookup"><span data-stu-id="1328e-102">MeasurePaulis operation</span></span>

<span data-ttu-id="1328e-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="1328e-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="1328e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1328e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1328e-105">Gezien een matrix met multi-Qubit Pauli-Opera Tors, meet elk met een opgegeven meet gadget en retourneert vervolgens de matrix met resultaten.</span><span class="sxs-lookup"><span data-stu-id="1328e-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="1328e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1328e-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="1328e-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="1328e-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="1328e-108">Matrix van multi-Qubit Pauli-Opera tors die moeten worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="1328e-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="1328e-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1328e-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1328e-110">Meld u aan om de gegeven Opera tors te meten.</span><span class="sxs-lookup"><span data-stu-id="1328e-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="1328e-111">Gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="1328e-111">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="1328e-112">Bewerking die de meting van een gegeven multi-Qubit-operator uitvoert.</span><span class="sxs-lookup"><span data-stu-id="1328e-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="1328e-113">Uitvoer: __ongeldig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="1328e-113">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="1328e-114">De matrix met resultaten die zijn verkregen van het meten van elk element van `paulis` op `target` .</span><span class="sxs-lookup"><span data-stu-id="1328e-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>