---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliMajIdx_
title: De functie _ZTermToPauliMajIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 13897d831bc3382dbb23b653c5905978330eb622
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214990"
---
# <a name="_ztermtopaulimajidx_-function"></a><span data-ttu-id="ae019-102">De functie _ZTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="ae019-102">_ZTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="ae019-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ae019-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ae019-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ae019-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ae019-105">Hiermee wordt een GeneratorIndex waarmee een Z-term wordt beschreven, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS.</span><span class="sxs-lookup"><span data-stu-id="ae019-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="ae019-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ae019-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="ae019-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ae019-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ae019-108">`GeneratorIndex` vertegenwoordigt een Z-term.</span><span class="sxs-lookup"><span data-stu-id="ae019-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="ae019-109">Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="ae019-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="ae019-110">' GeneratorIndex [] ' expressing Z-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="ae019-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>