---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliGenIdx_
title: De functie _V0123TermToPauliGenIdx_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: fc5ad0e97374c52a90012b0ce633af8488f3ad88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215092"
---
# <a name="_v0123termtopauligenidx_-function"></a><span data-ttu-id="939ec-102">De functie _V0123TermToPauliGenIdx_</span><span class="sxs-lookup"><span data-stu-id="939ec-102">_V0123TermToPauliGenIdx_ function</span></span>

<span data-ttu-id="939ec-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="939ec-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="939ec-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="939ec-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="939ec-105">Hiermee wordt een GeneratorIndex die een PQRS-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS</span><span class="sxs-lookup"><span data-stu-id="939ec-105">Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _V0123TermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="939ec-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="939ec-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="939ec-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="939ec-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="939ec-108">`GeneratorIndex` een PQRS-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="939ec-108">`GeneratorIndex` representing a PQRS term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="939ec-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="939ec-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="939ec-110">' GeneratorIndex [] ' expressing PQRS-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="939ec-110">'GeneratorIndex[]' expressing PQRS term as Pauli terms.</span></span>