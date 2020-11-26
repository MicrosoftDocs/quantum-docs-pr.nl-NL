---
uid: Microsoft.Quantum.Canon.BoundC
title: De functie BoundC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207578"
---
# <a name="boundc-function"></a><span data-ttu-id="1fca5-102">De functie BoundC</span><span class="sxs-lookup"><span data-stu-id="1fca5-102">BoundC function</span></span>

<span data-ttu-id="1fca5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1fca5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1fca5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fca5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fca5-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="1fca5-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="1fca5-106">De wijzigings functie `C` geeft aan dat alle bewerkingen in de matrix kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="1fca5-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="1fca5-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1fca5-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="1fca5-108">bewerkingen: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL []</span><span class="sxs-lookup"><span data-stu-id="1fca5-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="1fca5-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="1fca5-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="1fca5-110">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="1fca5-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1fca5-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="1fca5-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1fca5-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1fca5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1fca5-113">T</span><span class="sxs-lookup"><span data-stu-id="1fca5-113">'T</span></span>

<span data-ttu-id="1fca5-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="1fca5-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fca5-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1fca5-115">See Also</span></span>

- [<span data-ttu-id="1fca5-116">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="1fca5-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)