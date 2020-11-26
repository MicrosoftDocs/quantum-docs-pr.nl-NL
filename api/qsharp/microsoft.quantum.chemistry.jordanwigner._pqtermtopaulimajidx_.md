---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliMajIdx_
title: De functie _PQTermToPauliMajIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: bb9fad038c30b3362ffbecf546bcf85cb7dd13df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215398"
---
# <a name="_pqtermtopaulimajidx_-function"></a><span data-ttu-id="70917-102">De functie _PQTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="70917-102">_PQTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="70917-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="70917-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="70917-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="70917-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="70917-105">Hiermee wordt een GeneratorIndex die een PQ-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS</span><span class="sxs-lookup"><span data-stu-id="70917-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="70917-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="70917-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="70917-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="70917-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="70917-108">`GeneratorIndex` een PQ-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="70917-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="70917-109">Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="70917-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="70917-110">' GeneratorIndex [] ' expressing PQ-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="70917-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>