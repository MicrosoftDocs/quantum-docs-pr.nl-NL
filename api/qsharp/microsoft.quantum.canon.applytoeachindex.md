---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Bewerking ApplyToEachIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 4ce184b34add9238e26f9b35b40ec0bddb23ccf9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704956"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="d784a-102">Bewerking ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="d784a-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="d784a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d784a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d784a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d784a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d784a-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="d784a-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d784a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d784a-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="d784a-107">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d784a-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d784a-108">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="d784a-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="d784a-109">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="d784a-109">register : 'T[]</span></span>

<span data-ttu-id="d784a-110">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d784a-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d784a-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d784a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d784a-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d784a-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d784a-113">T</span><span class="sxs-lookup"><span data-stu-id="d784a-113">'T</span></span>

<span data-ttu-id="d784a-114">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="d784a-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="d784a-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d784a-115">See Also</span></span>

- [<span data-ttu-id="d784a-116">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="d784a-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="d784a-117">Micro soft. Quantum. Canon. ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="d784a-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="d784a-118">Micro soft. Quantum. Canon. ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="d784a-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="d784a-119">Micro soft. Quantum. Canon. ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="d784a-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)