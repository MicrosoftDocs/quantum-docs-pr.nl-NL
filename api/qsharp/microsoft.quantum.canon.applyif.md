---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Bewerking ApplyIf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: 109a5c4748d183f199e420b4b1aef687613d220c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841875"
---
# <a name="applyif-operation"></a><span data-ttu-id="4a9a9-102">Bewerking ApplyIf</span><span class="sxs-lookup"><span data-stu-id="4a9a9-102">ApplyIf operation</span></span>

<span data-ttu-id="4a9a9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4a9a9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a9a9-105">Past een bewerking toe die is voor een klassieke bit heeft gevoorwaardeeerd.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="4a9a9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4a9a9-106">Description</span></span>

<span data-ttu-id="4a9a9-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="4a9a9-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="4a9a9-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="4a9a9-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="4a9a9-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="4a9a9-110">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4a9a9-111">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="4a9a9-112">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4a9a9-113">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="4a9a9-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="4a9a9-114">target : 'T</span></span>

<span data-ttu-id="4a9a9-115">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4a9a9-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4a9a9-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="4a9a9-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4a9a9-118">T</span><span class="sxs-lookup"><span data-stu-id="4a9a9-118">'T</span></span>

<span data-ttu-id="4a9a9-119">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="4a9a9-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="4a9a9-120">Example</span></span>

<span data-ttu-id="4a9a9-121">Het volgende is een voor bereiding van een REGI ster van qubits in een verwerkings status die wordt vertegenwoordigd door een klassieke-bits teken reeks, gegeven als een matrix met `Bool` waarden:</span><span class="sxs-lookup"><span data-stu-id="4a9a9-121">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="4a9a9-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4a9a9-122">See Also</span></span>

- [<span data-ttu-id="4a9a9-123">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="4a9a9-123">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="4a9a9-124">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="4a9a9-124">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="4a9a9-125">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="4a9a9-125">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)