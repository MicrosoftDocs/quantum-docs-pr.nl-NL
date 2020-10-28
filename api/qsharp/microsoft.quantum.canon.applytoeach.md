---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Bewerking ApplyToEach
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704981"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="e5dfa-102">Bewerking ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="e5dfa-102">ApplyToEach operation</span></span>

<span data-ttu-id="e5dfa-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e5dfa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e5dfa-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5dfa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5dfa-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e5dfa-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e5dfa-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e5dfa-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="e5dfa-107">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5dfa-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e5dfa-108">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="e5dfa-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e5dfa-109">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="e5dfa-109">register : 'T[]</span></span>

<span data-ttu-id="e5dfa-110">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e5dfa-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5dfa-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5dfa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e5dfa-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e5dfa-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5dfa-113">T</span><span class="sxs-lookup"><span data-stu-id="e5dfa-113">'T</span></span>

<span data-ttu-id="e5dfa-114">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="e5dfa-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5dfa-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e5dfa-115">See Also</span></span>

- [<span data-ttu-id="e5dfa-116">Micro soft. Quantum. Canon. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="e5dfa-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="e5dfa-117">Micro soft. Quantum. Canon. ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="e5dfa-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="e5dfa-118">Micro soft. Quantum. Canon. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="e5dfa-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)