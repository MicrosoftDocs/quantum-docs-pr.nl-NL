---
uid: Microsoft.Quantum.Canon.BoundA
title: Functie bounda
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 40c112d0572dc4eebfc284c9ef29f43706e20c64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704468"
---
# <a name="bounda-function"></a><span data-ttu-id="5b2bc-102">Functie bounda</span><span class="sxs-lookup"><span data-stu-id="5b2bc-102">BoundA function</span></span>

<span data-ttu-id="5b2bc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5b2bc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5b2bc-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b2bc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b2bc-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="5b2bc-106">De wijzigings functie `A` geeft aan dat alle bewerkingen in de matrix adjointable zijn.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="5b2bc-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b2bc-107">Input</span></span>

### <a name="operations--t--unit-adj"></a><span data-ttu-id="5b2bc-108">bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ []</span><span class="sxs-lookup"><span data-stu-id="5b2bc-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="5b2bc-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="5b2bc-110">Output: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="5b2bc-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5b2bc-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5b2bc-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5b2bc-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5b2bc-113">T</span><span class="sxs-lookup"><span data-stu-id="5b2bc-113">'T</span></span>

<span data-ttu-id="5b2bc-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b2bc-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5b2bc-115">See Also</span></span>

- [<span data-ttu-id="5b2bc-116">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="5b2bc-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)