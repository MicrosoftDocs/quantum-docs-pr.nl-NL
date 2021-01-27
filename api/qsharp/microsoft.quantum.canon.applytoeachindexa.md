---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Bewerking ApplyToEachIndexA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: fb278f217ac450ab48aa37b0035cd1bdd295d3e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850831"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="e8e53-102">Bewerking ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="e8e53-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="e8e53-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8e53-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8e53-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8e53-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8e53-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e8e53-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="e8e53-106">De aanpassings functie `A` geeft aan dat de bewerking met één Qubit adjointable is.</span><span class="sxs-lookup"><span data-stu-id="e8e53-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="e8e53-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="e8e53-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="e8e53-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="e8e53-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e8e53-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="e8e53-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e8e53-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="e8e53-110">register : 'T[]</span></span>

<span data-ttu-id="e8e53-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e8e53-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8e53-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8e53-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e8e53-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e8e53-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8e53-114">T</span><span class="sxs-lookup"><span data-stu-id="e8e53-114">'T</span></span>

<span data-ttu-id="e8e53-115">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="e8e53-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8e53-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e8e53-116">See Also</span></span>

- [<span data-ttu-id="e8e53-117">Micro soft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="e8e53-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)