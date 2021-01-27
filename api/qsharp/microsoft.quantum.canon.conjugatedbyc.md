---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: De functie ConjugatedByC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 622b1d93dcbd02d000a68de23c66537b24d36c99
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840839"
---
# <a name="conjugatedbyc-function"></a><span data-ttu-id="3911c-102">De functie ConjugatedByC</span><span class="sxs-lookup"><span data-stu-id="3911c-102">ConjugatedByC function</span></span>

<span data-ttu-id="3911c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3911c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3911c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3911c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3911c-105">Als er buiten-en binnenste bewerkingen worden uitgevoerd, retourneert een nieuwe bewerking die de binnenste bewerking aan de buitenste bewerking heeft toegezien.</span><span class="sxs-lookup"><span data-stu-id="3911c-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="3911c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3911c-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="3911c-107">outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="3911c-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3911c-108">De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $.</span><span class="sxs-lookup"><span data-stu-id="3911c-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="3911c-109">Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="3911c-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-ctl"></a><span data-ttu-id="3911c-110">innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="3911c-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3911c-111">De bewerking $V $ wordt geconjugeerd.</span><span class="sxs-lookup"><span data-stu-id="3911c-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="3911c-112">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="3911c-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3911c-113">Een nieuwe bewerking waarvan de actie wordt vertegenwoordigd door de unitary $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="3911c-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3911c-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3911c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3911c-115">T</span><span class="sxs-lookup"><span data-stu-id="3911c-115">'T</span></span>

<span data-ttu-id="3911c-116">Het type doel waarop de interne en externe bewerkingen handelen.</span><span class="sxs-lookup"><span data-stu-id="3911c-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="3911c-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3911c-117">Remarks</span></span>

<span data-ttu-id="3911c-118">Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="3911c-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="3911c-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3911c-119">See Also</span></span>

- [<span data-ttu-id="3911c-120">Micro soft. Quantum. Canon. ConjugatedBy</span><span class="sxs-lookup"><span data-stu-id="3911c-120">Microsoft.Quantum.Canon.ConjugatedBy</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedBy)
- [<span data-ttu-id="3911c-121">Micro soft. Quantum. Canon. ConjugatedByA</span><span class="sxs-lookup"><span data-stu-id="3911c-121">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="3911c-122">Micro soft. Quantum. Canon. ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="3911c-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="3911c-123">Micro soft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="3911c-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)