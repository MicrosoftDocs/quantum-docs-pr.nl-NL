---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: De functie PauliStringFromGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230307"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="ea56b-102">De functie PauliStringFromGenIdx</span><span class="sxs-lookup"><span data-stu-id="ea56b-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="ea56b-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ea56b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ea56b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea56b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea56b-105">Extraheert de Pauli-teken reeks en de Qubit indices van een Pauli-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="ea56b-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="ea56b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ea56b-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="ea56b-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ea56b-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ea56b-108">`GeneratorIndex` type dat een Pauli-term codeert.</span><span class="sxs-lookup"><span data-stu-id="ea56b-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="ea56b-109">Output: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="ea56b-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="ea56b-110">De Pauli-teken reeks van de term die wordt beschreven door een `GeneratorIndex` , en indexen voor de qubits waarop deze wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ea56b-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>