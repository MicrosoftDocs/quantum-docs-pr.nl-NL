---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: De functie _PQTermToPauliGenIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 7f1794f9e46323ccf722407fb7ae82f73ed76e40
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215432"
---
# <a name="_pqtermtopauligenidx_-function"></a><span data-ttu-id="8a47d-102">De functie _PQTermToPauliGenIdx_</span><span class="sxs-lookup"><span data-stu-id="8a47d-102">_PQTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="8a47d-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8a47d-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8a47d-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8a47d-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8a47d-105">Hiermee wordt een GeneratorIndex die een PQ-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS</span><span class="sxs-lookup"><span data-stu-id="8a47d-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="8a47d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8a47d-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="8a47d-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8a47d-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8a47d-108">`GeneratorIndex` een PQ-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8a47d-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="8a47d-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="8a47d-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="8a47d-110">' GeneratorIndex [] ' expressing PQ-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="8a47d-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>