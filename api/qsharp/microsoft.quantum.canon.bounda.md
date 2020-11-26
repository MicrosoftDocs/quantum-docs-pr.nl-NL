---
uid: Microsoft.Quantum.Canon.BoundA
title: Functie bounda
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216945"
---
# <a name="bounda-function"></a><span data-ttu-id="489c5-102">Functie bounda</span><span class="sxs-lookup"><span data-stu-id="489c5-102">BoundA function</span></span>

<span data-ttu-id="489c5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="489c5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="489c5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="489c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="489c5-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="489c5-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="489c5-106">De wijzigings functie `A` geeft aan dat alle bewerkingen in de matrix adjointable zijn.</span><span class="sxs-lookup"><span data-stu-id="489c5-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="489c5-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="489c5-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="489c5-108">bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ []</span><span class="sxs-lookup"><span data-stu-id="489c5-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="489c5-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="489c5-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="489c5-110">Output: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="489c5-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="489c5-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="489c5-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="489c5-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="489c5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="489c5-113">T</span><span class="sxs-lookup"><span data-stu-id="489c5-113">'T</span></span>

<span data-ttu-id="489c5-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="489c5-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="489c5-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="489c5-115">See Also</span></span>

- [<span data-ttu-id="489c5-116">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="489c5-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)