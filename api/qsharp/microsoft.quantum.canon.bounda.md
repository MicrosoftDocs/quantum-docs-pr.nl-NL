---
uid: Microsoft.Quantum.Canon.BoundA
title: Functie bounda
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3d0a5ba5d3d9c76289ed29e59a9c226358b83797
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844543"
---
# <a name="bounda-function"></a><span data-ttu-id="5a033-102">Functie bounda</span><span class="sxs-lookup"><span data-stu-id="5a033-102">BoundA function</span></span>

<span data-ttu-id="5a033-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5a033-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5a033-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a033-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a033-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="5a033-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="5a033-106">De wijzigings functie `A` geeft aan dat alle bewerkingen in de matrix adjointable zijn.</span><span class="sxs-lookup"><span data-stu-id="5a033-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="5a033-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5a033-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="5a033-108">bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ []</span><span class="sxs-lookup"><span data-stu-id="5a033-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="5a033-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="5a033-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="5a033-110">Output: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="5a033-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5a033-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="5a033-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5a033-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5a033-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a033-113">T</span><span class="sxs-lookup"><span data-stu-id="5a033-113">'T</span></span>

<span data-ttu-id="5a033-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="5a033-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="5a033-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5a033-115">Example</span></span>

<span data-ttu-id="5a033-116">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="5a033-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundA([U, V]);
bound(x);
```

<span data-ttu-id="5a033-117">en</span><span class="sxs-lookup"><span data-stu-id="5a033-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="5a033-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5a033-118">See Also</span></span>

- [<span data-ttu-id="5a033-119">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="5a033-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)