---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Bewerking ApplyIf
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c5a1012328fa012ee02707aa59c94ac9c44b8e87
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218832"
---
# <a name="applyif-operation"></a><span data-ttu-id="30fbf-102">Bewerking ApplyIf</span><span class="sxs-lookup"><span data-stu-id="30fbf-102">ApplyIf operation</span></span>

<span data-ttu-id="30fbf-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="30fbf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="30fbf-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30fbf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30fbf-105">Past een bewerking toe die is voor een klassieke bit heeft gevoorwaardeeerd.</span><span class="sxs-lookup"><span data-stu-id="30fbf-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="30fbf-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="30fbf-106">Description</span></span>

<span data-ttu-id="30fbf-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="30fbf-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="30fbf-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="30fbf-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="30fbf-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="30fbf-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="30fbf-110">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30fbf-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="30fbf-111">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="30fbf-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="30fbf-112">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="30fbf-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="30fbf-113">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="30fbf-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="30fbf-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="30fbf-114">target : 'T</span></span>

<span data-ttu-id="30fbf-115">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="30fbf-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30fbf-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30fbf-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="30fbf-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="30fbf-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="30fbf-118">T</span><span class="sxs-lookup"><span data-stu-id="30fbf-118">'T</span></span>

<span data-ttu-id="30fbf-119">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="30fbf-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="30fbf-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="30fbf-120">See Also</span></span>

- [<span data-ttu-id="30fbf-121">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="30fbf-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="30fbf-122">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="30fbf-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="30fbf-123">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="30fbf-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)