---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: De functie ConjugatedByCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: acd5a9f796f751b9c9c374d841e80de9286fcd24
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207306"
---
# <a name="conjugatedbyca-function"></a><span data-ttu-id="7e258-102">De functie ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="7e258-102">ConjugatedByCA function</span></span>

<span data-ttu-id="7e258-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7e258-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7e258-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7e258-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7e258-105">Als er buiten-en binnenste bewerkingen worden uitgevoerd, retourneert een nieuwe bewerking die de binnenste bewerking aan de buitenste bewerking heeft toegezien.</span><span class="sxs-lookup"><span data-stu-id="7e258-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7e258-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7e258-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="7e258-107">outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="7e258-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7e258-108">De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $.</span><span class="sxs-lookup"><span data-stu-id="7e258-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="7e258-109">Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="7e258-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="7e258-110">innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="7e258-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7e258-111">De bewerking $V $ wordt geconjugeerd.</span><span class="sxs-lookup"><span data-stu-id="7e258-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="7e258-112">Output: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="7e258-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7e258-113">Een nieuwe bewerking waarvan de actie wordt vertegenwoordigd door de unitary $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="7e258-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7e258-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7e258-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7e258-115">T</span><span class="sxs-lookup"><span data-stu-id="7e258-115">'T</span></span>

<span data-ttu-id="7e258-116">Het type doel waarop de interne en externe bewerkingen handelen.</span><span class="sxs-lookup"><span data-stu-id="7e258-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e258-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7e258-117">Remarks</span></span>

<span data-ttu-id="7e258-118">Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="7e258-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e258-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7e258-119">See Also</span></span>

- [<span data-ttu-id="7e258-120">Micro soft. Quantum. Canon. ConjugatedByA</span><span class="sxs-lookup"><span data-stu-id="7e258-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="7e258-121">Micro soft. Quantum. Canon. ConjugatedByC</span><span class="sxs-lookup"><span data-stu-id="7e258-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="7e258-122">Micro soft. Quantum. Canon. ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="7e258-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="7e258-123">Micro soft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="7e258-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)