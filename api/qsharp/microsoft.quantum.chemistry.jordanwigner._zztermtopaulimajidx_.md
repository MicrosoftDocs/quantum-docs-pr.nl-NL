---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZZTermToPauliMajIdx_
title: De functie _ZZTermToPauliMajIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: ca713260da2dd717cb1548ef86b7faa0d1b826aa
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214922"
---
# <a name="_zztermtopaulimajidx_-function"></a><span data-ttu-id="67c73-102">De functie _ZZTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="67c73-102">_ZZTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="67c73-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="67c73-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="67c73-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="67c73-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="67c73-105">Hiermee wordt een GeneratorIndex die een ZZ-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS.</span><span class="sxs-lookup"><span data-stu-id="67c73-105">Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="67c73-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="67c73-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="67c73-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="67c73-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="67c73-108">`GeneratorIndex` vertegenwoordigt een ZZ-term.</span><span class="sxs-lookup"><span data-stu-id="67c73-108">`GeneratorIndex` representing a ZZ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="67c73-109">Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="67c73-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="67c73-110">' GeneratorIndex [] ' de ZZ-term wordt als Pauli-voor waarden Express.</span><span class="sxs-lookup"><span data-stu-id="67c73-110">'GeneratorIndex[]' expressing ZZ term as Pauli terms.</span></span>