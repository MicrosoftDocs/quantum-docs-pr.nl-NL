---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Bewerking ApplyIfCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: b0ac469d6dea51951e0d9b2cfceb54253d4b4c5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209618"
---
# <a name="applyifca-operation"></a><span data-ttu-id="dfdc8-102">Bewerking ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="dfdc8-102">ApplyIfCA operation</span></span>

<span data-ttu-id="dfdc8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dfdc8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dfdc8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dfdc8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dfdc8-105">Hiermee wordt een unitary bewerking toegepast die is voor bereid op een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="dfdc8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dfdc8-106">Description</span></span>

<span data-ttu-id="dfdc8-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="dfdc8-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="dfdc8-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="dfdc8-109">Het achtervoegsel `CA` geeft aan dat de bewerking die moet worden toegepast, unitary is (adjointable).</span><span class="sxs-lookup"><span data-stu-id="dfdc8-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="dfdc8-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="dfdc8-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="dfdc8-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="dfdc8-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dfdc8-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="dfdc8-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dfdc8-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dfdc8-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="dfdc8-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="dfdc8-115">target : 'T</span></span>

<span data-ttu-id="dfdc8-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfdc8-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfdc8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dfdc8-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dfdc8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dfdc8-119">T</span><span class="sxs-lookup"><span data-stu-id="dfdc8-119">'T</span></span>

<span data-ttu-id="dfdc8-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="dfdc8-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfdc8-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dfdc8-121">See Also</span></span>

- [<span data-ttu-id="dfdc8-122">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="dfdc8-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="dfdc8-123">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="dfdc8-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="dfdc8-124">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="dfdc8-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)