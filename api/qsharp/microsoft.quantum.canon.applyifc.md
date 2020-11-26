---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Bewerking ApplyIfC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: 35430cb7cf491965b7b69ace6d3f41599dbadd51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218713"
---
# <a name="applyifc-operation"></a><span data-ttu-id="27820-102">Bewerking ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="27820-102">ApplyIfC operation</span></span>

<span data-ttu-id="27820-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="27820-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="27820-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="27820-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="27820-105">Hiermee wordt een te bewerkte bewerking op een klassieke bit toegepast.</span><span class="sxs-lookup"><span data-stu-id="27820-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="27820-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="27820-106">Description</span></span>

<span data-ttu-id="27820-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="27820-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="27820-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="27820-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="27820-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="27820-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="27820-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="27820-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="27820-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="27820-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="27820-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="27820-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="27820-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="27820-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="27820-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="27820-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="27820-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="27820-115">target : 'T</span></span>

<span data-ttu-id="27820-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="27820-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="27820-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27820-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="27820-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="27820-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="27820-119">T</span><span class="sxs-lookup"><span data-stu-id="27820-119">'T</span></span>

<span data-ttu-id="27820-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="27820-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="27820-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="27820-121">See Also</span></span>

- [<span data-ttu-id="27820-122">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="27820-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="27820-123">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="27820-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="27820-124">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="27820-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)