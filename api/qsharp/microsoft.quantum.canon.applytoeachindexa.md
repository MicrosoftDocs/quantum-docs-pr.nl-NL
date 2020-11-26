---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Bewerking ApplyToEachIndexA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: e3ff812f14181e676fddf436af8a14f9a58271ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217591"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="49fee-102">Bewerking ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="49fee-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="49fee-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="49fee-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="49fee-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49fee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49fee-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="49fee-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="49fee-106">De aanpassings functie `A` geeft aan dat de bewerking met één Qubit adjointable is.</span><span class="sxs-lookup"><span data-stu-id="49fee-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="49fee-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="49fee-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="49fee-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="49fee-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="49fee-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="49fee-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="49fee-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="49fee-110">register : 'T[]</span></span>

<span data-ttu-id="49fee-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="49fee-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="49fee-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="49fee-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="49fee-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="49fee-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="49fee-114">T</span><span class="sxs-lookup"><span data-stu-id="49fee-114">'T</span></span>

<span data-ttu-id="49fee-115">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="49fee-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="49fee-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="49fee-116">See Also</span></span>

- [<span data-ttu-id="49fee-117">Micro soft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="49fee-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)