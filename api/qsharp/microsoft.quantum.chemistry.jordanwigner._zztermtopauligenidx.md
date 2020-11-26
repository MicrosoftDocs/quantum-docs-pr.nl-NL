---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZZTermToPauliGenIdx
title: Functie _ZZTermToPauliGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 01f4ebf4f2acc0fd76ae101e0c511cd70b03fada
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214956"
---
# <a name="_zztermtopauligenidx-function"></a><span data-ttu-id="9dbcb-102">Functie _ZZTermToPauliGenIdx</span><span class="sxs-lookup"><span data-stu-id="9dbcb-102">_ZZTermToPauliGenIdx function</span></span>

<span data-ttu-id="9dbcb-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="9dbcb-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="9dbcb-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="9dbcb-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="9dbcb-105">Hiermee wordt een GeneratorIndex die een ZZ-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-105">Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="9dbcb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9dbcb-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="9dbcb-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="9dbcb-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="9dbcb-108">`GeneratorIndex` vertegenwoordigt een ZZ-term.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-108">`GeneratorIndex` representing a ZZ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="9dbcb-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="9dbcb-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="9dbcb-110">' GeneratorIndex [] ' de ZZ-term wordt als Pauli-voor waarden Express.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-110">'GeneratorIndex[]' expressing ZZ term as Pauli terms.</span></span>