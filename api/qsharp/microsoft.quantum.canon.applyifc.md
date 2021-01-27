---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Bewerking ApplyIfC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: ef16b23349b604d174e72d9ae06d2052e2ab60f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841863"
---
# <a name="applyifc-operation"></a><span data-ttu-id="9e20f-102">Bewerking ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="9e20f-102">ApplyIfC operation</span></span>

<span data-ttu-id="9e20f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e20f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e20f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e20f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e20f-105">Hiermee wordt een te bewerkte bewerking op een klassieke bit toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e20f-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="9e20f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9e20f-106">Description</span></span>

<span data-ttu-id="9e20f-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="9e20f-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="9e20f-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="9e20f-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="9e20f-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="9e20f-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="9e20f-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e20f-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="9e20f-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9e20f-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9e20f-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e20f-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="9e20f-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9e20f-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9e20f-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="9e20f-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="9e20f-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="9e20f-115">target : 'T</span></span>

<span data-ttu-id="9e20f-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e20f-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9e20f-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9e20f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9e20f-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9e20f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e20f-119">T</span><span class="sxs-lookup"><span data-stu-id="9e20f-119">'T</span></span>

<span data-ttu-id="9e20f-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e20f-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="9e20f-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9e20f-121">Example</span></span>

<span data-ttu-id="9e20f-122">Het volgende is een voor bereiding van een REGI ster van qubits in een verwerkings status die wordt vertegenwoordigd door een klassieke-bits teken reeks, gegeven als een matrix met `Bool` waarden:</span><span class="sxs-lookup"><span data-stu-id="9e20f-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="9e20f-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9e20f-123">See Also</span></span>

- [<span data-ttu-id="9e20f-124">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="9e20f-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="9e20f-125">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="9e20f-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="9e20f-126">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="9e20f-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)