---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Bewerking ApplyToEachIndexC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: c005f616d580438891fbcb9f3c727b8e961e138d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850812"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="814cb-102">Bewerking ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="814cb-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="814cb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="814cb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="814cb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="814cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="814cb-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="814cb-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="814cb-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="814cb-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="814cb-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="814cb-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-ctl"></a><span data-ttu-id="814cb-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="814cb-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="814cb-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="814cb-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="814cb-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="814cb-110">register : 'T[]</span></span>

<span data-ttu-id="814cb-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="814cb-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="814cb-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="814cb-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="814cb-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="814cb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="814cb-114">T</span><span class="sxs-lookup"><span data-stu-id="814cb-114">'T</span></span>

<span data-ttu-id="814cb-115">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="814cb-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="814cb-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="814cb-116">See Also</span></span>

- [<span data-ttu-id="814cb-117">Micro soft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="814cb-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)