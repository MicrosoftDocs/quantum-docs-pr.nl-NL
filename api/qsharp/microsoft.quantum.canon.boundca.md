---
uid: Microsoft.Quantum.Canon.BoundCA
title: De functie BoundCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704436"
---
# <a name="boundca-function"></a><span data-ttu-id="1a2e9-102">De functie BoundCA</span><span class="sxs-lookup"><span data-stu-id="1a2e9-102">BoundCA function</span></span>

<span data-ttu-id="1a2e9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1a2e9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1a2e9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1a2e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1a2e9-105">Op basis van een matrix van bewerkingen die worden uitgevoerd op één invoer, produceert een nieuwe bewerking die elke opgegeven bewerking in volg orde uitvoert.</span><span class="sxs-lookup"><span data-stu-id="1a2e9-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="1a2e9-106">De wijzigings functie `CA` geeft aan dat alle bewerkingen in de matrix adjointable en bewerkbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="1a2e9-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1a2e9-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1a2e9-107">Input</span></span>

### <a name="operations--t--unit-adj--ctl"></a><span data-ttu-id="1a2e9-108">bewerkingen: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="1a2e9-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="1a2e9-109">Een reeks bewerkingen die moeten worden uitgevoerd op een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="1a2e9-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj--ctl"></a><span data-ttu-id="1a2e9-110">Output: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="1a2e9-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="1a2e9-111">Een nieuwe bewerking waarbij elke opgegeven bewerking wordt uitgevoerd in de volg orde van de invoer.</span><span class="sxs-lookup"><span data-stu-id="1a2e9-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1a2e9-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1a2e9-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1a2e9-113">T</span><span class="sxs-lookup"><span data-stu-id="1a2e9-113">'T</span></span>

<span data-ttu-id="1a2e9-114">Het doel waarop elk van de bewerkingen in de matrix Act.</span><span class="sxs-lookup"><span data-stu-id="1a2e9-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a2e9-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a2e9-115">See Also</span></span>

- [<span data-ttu-id="1a2e9-116">Micro soft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="1a2e9-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)