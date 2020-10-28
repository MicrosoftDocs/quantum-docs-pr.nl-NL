---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Bewerking ApplyIf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c8f6860a7a3b8af86b0edb048baccbf057dd245a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705357"
---
# <a name="applyif-operation"></a><span data-ttu-id="df731-102">Bewerking ApplyIf</span><span class="sxs-lookup"><span data-stu-id="df731-102">ApplyIf operation</span></span>

<span data-ttu-id="df731-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="df731-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="df731-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df731-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df731-105">Past een bewerking toe die is voor een klassieke bit heeft gevoorwaardeeerd.</span><span class="sxs-lookup"><span data-stu-id="df731-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="df731-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="df731-106">Description</span></span>

<span data-ttu-id="df731-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="df731-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="df731-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="df731-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="df731-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="df731-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="df731-110">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df731-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="df731-111">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="df731-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="df731-112">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="df731-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="df731-113">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="df731-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="df731-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="df731-114">target : 'T</span></span>

<span data-ttu-id="df731-115">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="df731-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df731-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df731-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="df731-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="df731-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df731-118">T</span><span class="sxs-lookup"><span data-stu-id="df731-118">'T</span></span>

<span data-ttu-id="df731-119">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="df731-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="df731-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="df731-120">See Also</span></span>

- [<span data-ttu-id="df731-121">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="df731-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="df731-122">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="df731-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="df731-123">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="df731-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)