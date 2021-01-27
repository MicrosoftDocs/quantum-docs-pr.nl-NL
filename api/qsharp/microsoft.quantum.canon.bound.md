---
uid: Microsoft.Quantum.Canon.Bound
title: Gebonden functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841055"
---
# <a name="bound-function"></a><span data-ttu-id="98493-102">Gebonden functie</span><span class="sxs-lookup"><span data-stu-id="98493-102">Bound function</span></span>

<span data-ttu-id="98493-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="98493-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="98493-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="98493-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="98493-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="98493-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="98493-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="98493-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="98493-107">bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="98493-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="98493-108">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="98493-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="98493-109">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98493-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="98493-110">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="98493-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="98493-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="98493-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="98493-112">T</span><span class="sxs-lookup"><span data-stu-id="98493-112">'T</span></span>

<span data-ttu-id="98493-113">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="98493-113">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="98493-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="98493-114">Example</span></span>

<span data-ttu-id="98493-115">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="98493-115">The following are equivalent:</span></span>

```qsharp
let bound = Bound([U, V]);
bound(x);
```

<span data-ttu-id="98493-116">en</span><span class="sxs-lookup"><span data-stu-id="98493-116">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="98493-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="98493-117">See Also</span></span>

- [<span data-ttu-id="98493-118">Micro soft. Quantum. Canon. BoundC</span><span class="sxs-lookup"><span data-stu-id="98493-118">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="98493-119">Micro soft. Quantum. Canon. Bounda</span><span class="sxs-lookup"><span data-stu-id="98493-119">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="98493-120">Micro soft. Quantum. Canon. BoundCA</span><span class="sxs-lookup"><span data-stu-id="98493-120">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)