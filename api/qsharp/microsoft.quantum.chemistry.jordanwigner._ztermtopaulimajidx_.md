---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliMajIdx_
title: De functie _ZTermToPauliMajIdx_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 890e60c4b7c5bc474c9f00b59dac6bfddb0e891b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703257"
---
# <a name="_ztermtopaulimajidx_-function"></a><span data-ttu-id="b65d9-102">De functie _ZTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="b65d9-102">_ZTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="b65d9-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b65d9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b65d9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b65d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b65d9-105">Hiermee wordt een GeneratorIndex waarmee een Z-term wordt beschreven, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS.</span><span class="sxs-lookup"><span data-stu-id="b65d9-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="b65d9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b65d9-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="b65d9-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b65d9-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="b65d9-108">`GeneratorIndex` vertegenwoordigt een Z-term.</span><span class="sxs-lookup"><span data-stu-id="b65d9-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="b65d9-109">Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="b65d9-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="b65d9-110">' GeneratorIndex [] ' expressing Z-term als Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="b65d9-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>