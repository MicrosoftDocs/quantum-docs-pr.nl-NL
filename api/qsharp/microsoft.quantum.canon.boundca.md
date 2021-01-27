---
uid: Microsoft.Quantum.Canon.BoundCA
title: De functie BoundCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844520"
---
# <a name="boundca-function"></a><span data-ttu-id="06cb3-102">De functie BoundCA</span><span class="sxs-lookup"><span data-stu-id="06cb3-102">BoundCA function</span></span>

<span data-ttu-id="06cb3-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="06cb3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="06cb3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06cb3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06cb3-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="06cb3-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="06cb3-106">De wijzigings functie `CA` geeft aan dat alle bewerkingen in de matrix adjointable en bewerkbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="06cb3-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="06cb3-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="06cb3-107">Input</span></span>

### <a name="operations--t--unit--is-adj--ctl"></a><span data-ttu-id="06cb3-108">bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []</span><span class="sxs-lookup"><span data-stu-id="06cb3-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="06cb3-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="06cb3-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="06cb3-110">Output: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="06cb3-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="06cb3-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="06cb3-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="06cb3-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="06cb3-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="06cb3-113">T</span><span class="sxs-lookup"><span data-stu-id="06cb3-113">'T</span></span>

<span data-ttu-id="06cb3-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="06cb3-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="06cb3-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="06cb3-115">Example</span></span>

<span data-ttu-id="06cb3-116">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="06cb3-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

<span data-ttu-id="06cb3-117">en</span><span class="sxs-lookup"><span data-stu-id="06cb3-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="06cb3-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="06cb3-118">See Also</span></span>

- [<span data-ttu-id="06cb3-119">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="06cb3-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)