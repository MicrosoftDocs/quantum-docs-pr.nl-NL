---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliGenIdx
title: Functie _ZTermToPauliGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: f4643ef03a0178f2c3ba1ea68f36f2f3fcd7b9ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215024"
---
# <a name="_ztermtopauligenidx-function"></a><span data-ttu-id="0949a-102">Functie _ZTermToPauliGenIdx</span><span class="sxs-lookup"><span data-stu-id="0949a-102">_ZTermToPauliGenIdx function</span></span>

<span data-ttu-id="0949a-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="0949a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="0949a-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="0949a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="0949a-105">Hiermee wordt een GeneratorIndex waarmee een Z-term wordt beschreven, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS.</span><span class="sxs-lookup"><span data-stu-id="0949a-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="0949a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0949a-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="0949a-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="0949a-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="0949a-108">`GeneratorIndex` vertegenwoordigt een Z-term.</span><span class="sxs-lookup"><span data-stu-id="0949a-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="0949a-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="0949a-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="0949a-110">' GeneratorIndex [] ' expressing Z-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="0949a-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>