---
uid: Microsoft.Quantum.Canon.BoundC
title: De functie BoundC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 6b640c0dab14778336f42098e699e7e68cc726df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841045"
---
# <a name="boundc-function"></a><span data-ttu-id="d6623-102">De functie BoundC</span><span class="sxs-lookup"><span data-stu-id="d6623-102">BoundC function</span></span>

<span data-ttu-id="d6623-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d6623-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d6623-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6623-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6623-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d6623-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="d6623-106">De wijzigings functie `C` geeft aan dat alle bewerkingen in de matrix kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="d6623-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="d6623-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="d6623-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="d6623-108">bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL []</span><span class="sxs-lookup"><span data-stu-id="d6623-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="d6623-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="d6623-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="d6623-110">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="d6623-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="d6623-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="d6623-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d6623-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d6623-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d6623-113">T</span><span class="sxs-lookup"><span data-stu-id="d6623-113">'T</span></span>

<span data-ttu-id="d6623-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="d6623-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="d6623-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d6623-115">Example</span></span>

<span data-ttu-id="d6623-116">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d6623-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundC([U, V]);
bound(x);
```

<span data-ttu-id="d6623-117">en</span><span class="sxs-lookup"><span data-stu-id="d6623-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="d6623-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d6623-118">See Also</span></span>

- [<span data-ttu-id="d6623-119">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="d6623-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)