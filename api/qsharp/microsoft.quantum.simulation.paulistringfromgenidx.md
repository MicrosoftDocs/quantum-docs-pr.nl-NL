---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: De functie PauliStringFromGenIdx
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 048f91411099d24f3c0c5fd8ae3703779e7ab8a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847916"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="a955d-102">De functie PauliStringFromGenIdx</span><span class="sxs-lookup"><span data-stu-id="a955d-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="a955d-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a955d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a955d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a955d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a955d-105">Extraheert de Pauli-teken reeks en de Qubit indices van een Pauli-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="a955d-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="a955d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a955d-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="a955d-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="a955d-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="a955d-108">`GeneratorIndex` type dat een Pauli-term codeert.</span><span class="sxs-lookup"><span data-stu-id="a955d-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="a955d-109">Output: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="a955d-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="a955d-110">De Pauli-teken reeks van de term die wordt beschreven door een `GeneratorIndex` , en indexen voor de qubits waarop deze wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a955d-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>