---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Bewerking ApplySeriesOfOps
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: aff0bcb831960153166e88aef1f05e000125d5d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705028"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="d8a91-102">Bewerking ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="d8a91-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="d8a91-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d8a91-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d8a91-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d8a91-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d8a91-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="d8a91-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d8a91-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d8a91-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="d8a91-107">listOfOps: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="d8a91-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="d8a91-108">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8a91-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="d8a91-109">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8a91-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="d8a91-110">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="d8a91-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="d8a91-111">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="d8a91-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="d8a91-112">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d8a91-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="d8a91-113">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="d8a91-113">register : 'T[]</span></span>

<span data-ttu-id="d8a91-114">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="d8a91-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d8a91-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d8a91-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d8a91-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d8a91-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d8a91-117">T</span><span class="sxs-lookup"><span data-stu-id="d8a91-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="d8a91-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d8a91-118">See Also</span></span>

- [<span data-ttu-id="d8a91-119">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="d8a91-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)