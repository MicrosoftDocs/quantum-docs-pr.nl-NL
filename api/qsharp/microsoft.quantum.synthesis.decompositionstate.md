---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Door de gebruiker gedefinieerd DecompositionState-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: eb2aed53b4116a4ea72ee732ff46c4a10eb3d67b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855509"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="054fe-102">Door de gebruiker gedefinieerd DecompositionState-type</span><span class="sxs-lookup"><span data-stu-id="054fe-102">DecompositionState user defined type</span></span>

<span data-ttu-id="054fe-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="054fe-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="054fe-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="054fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="054fe-105">Status tijdens het desamen stellen op basis van variabelen indexen</span><span class="sxs-lookup"><span data-stu-id="054fe-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="054fe-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="054fe-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="054fe-107">Macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="054fe-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="054fe-108">Lfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="054fe-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="054fe-109">Rfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="054fe-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="054fe-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="054fe-110">Description</span></span>

<span data-ttu-id="054fe-111">De status bevat de huidige permutatie en de momenteel gegenereerde functies voor bewaakte Gates aan de linkerkant en beheerde poorten aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="054fe-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>