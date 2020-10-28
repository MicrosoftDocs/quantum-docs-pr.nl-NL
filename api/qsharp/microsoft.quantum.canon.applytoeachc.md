---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Bewerking ApplyToEachC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704965"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="3ec6b-102">Bewerking ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="3ec6b-102">ApplyToEachC operation</span></span>

<span data-ttu-id="3ec6b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3ec6b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3ec6b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3ec6b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3ec6b-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="3ec6b-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="3ec6b-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="3ec6b-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3ec6b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ec6b-107">Input</span></span>

### <a name="singleelementoperation--t--unit-ctl"></a><span data-ttu-id="3ec6b-108">singleElementOperation: 'T = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ec6b-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="3ec6b-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="3ec6b-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="3ec6b-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="3ec6b-110">register : 'T[]</span></span>

<span data-ttu-id="3ec6b-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="3ec6b-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ec6b-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ec6b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3ec6b-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3ec6b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3ec6b-114">T</span><span class="sxs-lookup"><span data-stu-id="3ec6b-114">'T</span></span>

<span data-ttu-id="3ec6b-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="3ec6b-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ec6b-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ec6b-116">See Also</span></span>

- [<span data-ttu-id="3ec6b-117">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="3ec6b-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)