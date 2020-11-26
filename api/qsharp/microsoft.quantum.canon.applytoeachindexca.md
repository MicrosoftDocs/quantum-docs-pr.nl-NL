---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Bewerking ApplyToEachIndexCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208938"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="1f702-102">Bewerking ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="1f702-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="1f702-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1f702-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1f702-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f702-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f702-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="1f702-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="1f702-106">De aanpassings functie `CA` geeft aan dat de bewerking met één Qubit adjointable en kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="1f702-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1f702-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1f702-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="1f702-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="1f702-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1f702-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="1f702-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1f702-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="1f702-110">register : 'T[]</span></span>

<span data-ttu-id="1f702-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1f702-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f702-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f702-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1f702-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1f702-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1f702-114">T</span><span class="sxs-lookup"><span data-stu-id="1f702-114">'T</span></span>

<span data-ttu-id="1f702-115">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="1f702-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f702-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1f702-116">See Also</span></span>

- [<span data-ttu-id="1f702-117">Micro soft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="1f702-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)