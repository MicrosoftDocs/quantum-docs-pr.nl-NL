---
uid: Microsoft.Quantum.Canon.Bound
title: Gebonden functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704476"
---
# <a name="bound-function"></a><span data-ttu-id="7249d-102">Gebonden functie</span><span class="sxs-lookup"><span data-stu-id="7249d-102">Bound function</span></span>

<span data-ttu-id="7249d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7249d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7249d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7249d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7249d-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="7249d-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="7249d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7249d-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="7249d-107">bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="7249d-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="7249d-108">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="7249d-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="7249d-109">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7249d-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7249d-110">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="7249d-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7249d-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7249d-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7249d-112">T</span><span class="sxs-lookup"><span data-stu-id="7249d-112">'T</span></span>

<span data-ttu-id="7249d-113">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="7249d-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="7249d-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7249d-114">See Also</span></span>

- [<span data-ttu-id="7249d-115">Micro soft. Quantum. Canon. BoundC</span><span class="sxs-lookup"><span data-stu-id="7249d-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="7249d-116">Micro soft. Quantum. Canon. Bounda</span><span class="sxs-lookup"><span data-stu-id="7249d-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="7249d-117">Micro soft. Quantum. Canon. BoundCA</span><span class="sxs-lookup"><span data-stu-id="7249d-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)