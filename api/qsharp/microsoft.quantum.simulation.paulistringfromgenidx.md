---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: De functie PauliStringFromGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 33da4bc3d7e58b87aef75b453b6af09a51214923
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701714"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="5f95b-102">De functie PauliStringFromGenIdx</span><span class="sxs-lookup"><span data-stu-id="5f95b-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="5f95b-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5f95b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5f95b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5f95b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5f95b-105">Extraheert de Pauli-teken reeks en de Qubit indices van een Pauli-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="5f95b-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="5f95b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5f95b-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="5f95b-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="5f95b-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="5f95b-108">`GeneratorIndex` type dat een Pauli-term codeert.</span><span class="sxs-lookup"><span data-stu-id="5f95b-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="5f95b-109">Output: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="5f95b-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="5f95b-110">De Pauli-teken reeks van de term die wordt beschreven door een `GeneratorIndex` , en indexen voor de qubits waarop deze wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5f95b-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>