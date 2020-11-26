---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliMajIdx_
title: De functie _V0123TermToPauliMajIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 0dd7faf6ce2948af57304e1c752d89384cc3ddbf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215058"
---
# <a name="_v0123termtopaulimajidx_-function"></a><span data-ttu-id="8d67c-102">De functie _V0123TermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="8d67c-102">_V0123TermToPauliMajIdx_ function</span></span>

<span data-ttu-id="8d67c-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8d67c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8d67c-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8d67c-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8d67c-105">Hiermee wordt een GeneratorIndex die een PQRS-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS</span><span class="sxs-lookup"><span data-stu-id="8d67c-105">Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _V0123TermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex[]
```


## <a name="input"></a><span data-ttu-id="8d67c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8d67c-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="8d67c-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8d67c-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8d67c-108">`GeneratorIndex` een PQRS-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8d67c-108">`GeneratorIndex` representing a PQRS term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="8d67c-109">Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)[]</span><span class="sxs-lookup"><span data-stu-id="8d67c-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)[]</span></span>

<span data-ttu-id="8d67c-110">' GeneratorIndex [] ' expressing PQRS-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="8d67c-110">'GeneratorIndex[]' expressing PQRS term as Pauli terms.</span></span>