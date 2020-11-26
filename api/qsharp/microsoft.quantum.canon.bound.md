---
uid: Microsoft.Quantum.Canon.Bound
title: Gebonden functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207595"
---
# <a name="bound-function"></a><span data-ttu-id="3e686-102">Gebonden functie</span><span class="sxs-lookup"><span data-stu-id="3e686-102">Bound function</span></span>

<span data-ttu-id="3e686-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3e686-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3e686-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e686-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e686-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="3e686-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="3e686-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3e686-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="3e686-107">bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="3e686-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="3e686-108">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="3e686-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="3e686-109">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e686-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="3e686-110">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="3e686-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3e686-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3e686-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3e686-112">T</span><span class="sxs-lookup"><span data-stu-id="3e686-112">'T</span></span>

<span data-ttu-id="3e686-113">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="3e686-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e686-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3e686-114">See Also</span></span>

- [<span data-ttu-id="3e686-115">Micro soft. Quantum. Canon. BoundC</span><span class="sxs-lookup"><span data-stu-id="3e686-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="3e686-116">Micro soft. Quantum. Canon. Bounda</span><span class="sxs-lookup"><span data-stu-id="3e686-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="3e686-117">Micro soft. Quantum. Canon. BoundCA</span><span class="sxs-lookup"><span data-stu-id="3e686-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)