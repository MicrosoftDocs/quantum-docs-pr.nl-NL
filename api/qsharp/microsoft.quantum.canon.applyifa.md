---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Bewerking ApplyIfA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: d2880bbb95ebaf621ef9e5885051b94f32a3f1cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218764"
---
# <a name="applyifa-operation"></a><span data-ttu-id="ae176-102">Bewerking ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="ae176-102">ApplyIfA operation</span></span>

<span data-ttu-id="ae176-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae176-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae176-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae176-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae176-105">Hiermee wordt een adjointable bewerking toegepast die is voor bereid op een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="ae176-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="ae176-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ae176-106">Description</span></span>

<span data-ttu-id="ae176-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="ae176-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="ae176-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="ae176-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="ae176-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="ae176-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="ae176-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="ae176-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="ae176-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="ae176-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ae176-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ae176-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="ae176-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ae176-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ae176-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="ae176-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="ae176-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="ae176-115">target : 'T</span></span>

<span data-ttu-id="ae176-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="ae176-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae176-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae176-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ae176-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ae176-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae176-119">T</span><span class="sxs-lookup"><span data-stu-id="ae176-119">'T</span></span>

<span data-ttu-id="ae176-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ae176-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae176-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ae176-121">See Also</span></span>

- [<span data-ttu-id="ae176-122">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="ae176-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="ae176-123">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="ae176-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="ae176-124">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="ae176-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)