---
uid: Microsoft.Quantum.Canon.BoundC
title: De functie BoundC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704453"
---
# <a name="boundc-function"></a><span data-ttu-id="698e4-102">De functie BoundC</span><span class="sxs-lookup"><span data-stu-id="698e4-102">BoundC function</span></span>

<span data-ttu-id="698e4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="698e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="698e4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="698e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="698e4-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="698e4-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="698e4-106">De wijzigings functie `C` geeft aan dat alle bewerkingen in de matrix kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="698e4-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="698e4-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="698e4-107">Input</span></span>

### <a name="operations--t--unit-ctl"></a><span data-ttu-id="698e4-108">bewerkingen: 'T = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="698e4-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="698e4-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="698e4-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="698e4-110">Output: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="698e4-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="698e4-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="698e4-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="698e4-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="698e4-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="698e4-113">T</span><span class="sxs-lookup"><span data-stu-id="698e4-113">'T</span></span>

<span data-ttu-id="698e4-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="698e4-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="698e4-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="698e4-115">See Also</span></span>

- [<span data-ttu-id="698e4-116">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="698e4-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)