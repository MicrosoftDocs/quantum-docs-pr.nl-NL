---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: Bewerking ApplyWithA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: f1ff31da53952931426d358cbedad44a50d87f5e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704604"
---
# <a name="applywitha-operation"></a><span data-ttu-id="e3b5c-102">Bewerking ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="e3b5c-102">ApplyWithA operation</span></span>

<span data-ttu-id="e3b5c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e3b5c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e3b5c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e3b5c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e3b5c-105">Als er twee bewerkingen worden uitgevoerd, geldt er een als conjugaat met de andere.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="e3b5c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e3b5c-106">Description</span></span>

<span data-ttu-id="e3b5c-107">Als er twee bewerkingen worden uitgevoerd, die respectievelijk worden beschreven door unitary Opera tors $U $ en $V $, worden deze toegepast in de volg orde $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="e3b5c-108">Dat wil zeggen dat met deze bewerking de unitary-operator wordt geïmplementeerd die is opgegeven door $V $ geconjugeerde met $U $.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="e3b5c-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="e3b5c-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="e3b5c-110">outerOperation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="e3b5c-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="e3b5c-111">De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="e3b5c-112">Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj"></a><span data-ttu-id="e3b5c-113">innerOperation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="e3b5c-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="e3b5c-114">De bewerking $V $ wordt geconjugeerd.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="e3b5c-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="e3b5c-115">target : 'T</span></span>

<span data-ttu-id="e3b5c-116">De invoer die moet worden opgegeven voor de buiten-en de binnenste bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3b5c-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3b5c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e3b5c-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e3b5c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3b5c-119">T</span><span class="sxs-lookup"><span data-stu-id="e3b5c-119">'T</span></span>

<span data-ttu-id="e3b5c-120">Het doel waarop elk van de interne en externe bewerkingen handelen.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b5c-121">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e3b5c-121">Remarks</span></span>

<span data-ttu-id="e3b5c-122">Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="e3b5c-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3b5c-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e3b5c-123">See Also</span></span>

- [<span data-ttu-id="e3b5c-124">Micro soft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="e3b5c-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="e3b5c-125">Micro soft. Quantum. Canon. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="e3b5c-125">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [<span data-ttu-id="e3b5c-126">Micro soft. Quantum. Canon. ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="e3b5c-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)