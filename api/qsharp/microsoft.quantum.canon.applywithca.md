---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Bewerking ApplyWithCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: a5ce7dc5ddfbb2fc06743d36614129c371850da2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841149"
---
# <a name="applywithca-operation"></a><span data-ttu-id="0d9bb-102">Bewerking ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="0d9bb-102">ApplyWithCA operation</span></span>

<span data-ttu-id="0d9bb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0d9bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0d9bb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0d9bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0d9bb-105">Als er twee bewerkingen worden uitgevoerd, geldt er een als conjugaat met de andere.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="0d9bb-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0d9bb-106">Description</span></span>

<span data-ttu-id="0d9bb-107">Als er twee bewerkingen worden uitgevoerd, die respectievelijk worden beschreven door unitary Opera tors $U $ en $V $, worden deze toegepast in de volg orde $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="0d9bb-108">Dat wil zeggen dat met deze bewerking de unitary-operator wordt geïmplementeerd die is opgegeven door $V $ geconjugeerde met $U $.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="0d9bb-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="0d9bb-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="0d9bb-110">outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="0d9bb-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="0d9bb-111">De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="0d9bb-112">Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="0d9bb-113">innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="0d9bb-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0d9bb-114">De bewerking $V $ wordt geconjugeerd.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="0d9bb-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="0d9bb-115">target : 'T</span></span>

<span data-ttu-id="0d9bb-116">De invoer die moet worden opgegeven voor de buiten-en de binnenste bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d9bb-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d9bb-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0d9bb-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="0d9bb-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0d9bb-119">T</span><span class="sxs-lookup"><span data-stu-id="0d9bb-119">'T</span></span>

<span data-ttu-id="0d9bb-120">Het doel waarop elk van de interne en externe bewerkingen handelen.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d9bb-121">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0d9bb-121">Remarks</span></span>

<span data-ttu-id="0d9bb-122">Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="0d9bb-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d9bb-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0d9bb-123">See Also</span></span>

- [<span data-ttu-id="0d9bb-124">Micro soft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="0d9bb-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="0d9bb-125">Micro soft. Quantum. Canon. ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="0d9bb-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="0d9bb-126">Micro soft. Quantum. Canon. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="0d9bb-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)