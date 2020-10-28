---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Bewerking ApplyIfA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: 279a069176ee24ed83406f72170462bf58c790d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705364"
---
# <a name="applyifa-operation"></a><span data-ttu-id="2e260-102">Bewerking ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="2e260-102">ApplyIfA operation</span></span>

<span data-ttu-id="2e260-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2e260-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2e260-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e260-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e260-105">Hiermee wordt een adjointable bewerking toegepast die is voor bereid op een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="2e260-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="2e260-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2e260-106">Description</span></span>

<span data-ttu-id="2e260-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="2e260-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="2e260-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="2e260-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="2e260-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="2e260-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="2e260-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="2e260-110">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="2e260-111">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="2e260-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="2e260-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="2e260-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="2e260-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2e260-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2e260-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="2e260-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="2e260-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="2e260-115">target : 'T</span></span>

<span data-ttu-id="2e260-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="2e260-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e260-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e260-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2e260-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2e260-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e260-119">T</span><span class="sxs-lookup"><span data-stu-id="2e260-119">'T</span></span>

<span data-ttu-id="2e260-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="2e260-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e260-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2e260-121">See Also</span></span>

- [<span data-ttu-id="2e260-122">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="2e260-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="2e260-123">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="2e260-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="2e260-124">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="2e260-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)