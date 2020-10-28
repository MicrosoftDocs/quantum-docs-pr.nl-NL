---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Bewerking ApplyToEachCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704957"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="f5e06-102">Bewerking ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="f5e06-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="f5e06-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f5e06-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f5e06-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f5e06-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f5e06-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f5e06-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f5e06-106">De aanpassings functie `CA` geeft aan dat de bewerking met één qubit kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="f5e06-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f5e06-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f5e06-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj--ctl"></a><span data-ttu-id="f5e06-108">singleElementOperation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f5e06-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f5e06-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="f5e06-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f5e06-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="f5e06-110">register : 'T[]</span></span>

<span data-ttu-id="f5e06-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f5e06-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f5e06-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f5e06-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f5e06-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f5e06-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f5e06-114">T</span><span class="sxs-lookup"><span data-stu-id="f5e06-114">'T</span></span>

<span data-ttu-id="f5e06-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="f5e06-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5e06-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f5e06-116">See Also</span></span>

- [<span data-ttu-id="f5e06-117">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="f5e06-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)