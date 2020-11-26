---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Bewerking ApplyToEachC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 535f815503e20b5cee35f3f273a714203a4baf12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217778"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="ce654-102">Bewerking ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="ce654-102">ApplyToEachC operation</span></span>

<span data-ttu-id="ce654-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce654-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce654-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce654-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce654-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="ce654-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="ce654-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="ce654-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ce654-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="ce654-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="ce654-108">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="ce654-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ce654-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="ce654-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="ce654-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="ce654-110">register : 'T[]</span></span>

<span data-ttu-id="ce654-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ce654-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce654-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce654-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ce654-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ce654-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce654-114">T</span><span class="sxs-lookup"><span data-stu-id="ce654-114">'T</span></span>

<span data-ttu-id="ce654-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="ce654-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce654-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ce654-116">See Also</span></span>

- [<span data-ttu-id="ce654-117">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="ce654-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)