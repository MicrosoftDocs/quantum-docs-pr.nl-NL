---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Door de gebruiker gedefinieerd DecompositionState-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709169"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="3c15b-102">Door de gebruiker gedefinieerd DecompositionState-type</span><span class="sxs-lookup"><span data-stu-id="3c15b-102">DecompositionState user defined type</span></span>

<span data-ttu-id="3c15b-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="3c15b-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="3c15b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3c15b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3c15b-105">Status tijdens het desamen stellen op basis van variabelen indexen</span><span class="sxs-lookup"><span data-stu-id="3c15b-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="3c15b-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="3c15b-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="3c15b-107">Macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3c15b-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="3c15b-108">Lfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="3c15b-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="3c15b-109">Rfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="3c15b-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="3c15b-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3c15b-110">Description</span></span>

<span data-ttu-id="3c15b-111">De status bevat de huidige permutatie en de momenteel gegenereerde functies voor bewaakte Gates aan de linkerkant en beheerde poorten aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="3c15b-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>