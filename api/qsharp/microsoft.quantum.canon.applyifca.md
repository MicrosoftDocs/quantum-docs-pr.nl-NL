---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Bewerking ApplyIfCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: b9d5e2c6868dc7b876917abf28f68bb5d0d0f2f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845009"
---
# <a name="applyifca-operation"></a><span data-ttu-id="a233c-102">Bewerking ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="a233c-102">ApplyIfCA operation</span></span>

<span data-ttu-id="a233c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a233c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a233c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a233c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a233c-105">Hiermee wordt een unitary bewerking toegepast die is voor bereid op een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="a233c-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a233c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a233c-106">Description</span></span>

<span data-ttu-id="a233c-107">Gezien een bewerking `op` en een bitlengte `bit` , geldt `op` voor de `target` if `bit` `true` -waarde.</span><span class="sxs-lookup"><span data-stu-id="a233c-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="a233c-108">Als `false` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="a233c-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="a233c-109">Het achtervoegsel `CA` geeft aan dat de bewerking die moet worden toegepast, unitary is (adjointable).</span><span class="sxs-lookup"><span data-stu-id="a233c-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="a233c-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="a233c-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a233c-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="a233c-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a233c-112">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a233c-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="a233c-113">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a233c-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a233c-114">een Booleaanse waarde die bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="a233c-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="a233c-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="a233c-115">target : 'T</span></span>

<span data-ttu-id="a233c-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a233c-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a233c-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a233c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a233c-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a233c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a233c-119">T</span><span class="sxs-lookup"><span data-stu-id="a233c-119">'T</span></span>

<span data-ttu-id="a233c-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a233c-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="a233c-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a233c-121">Example</span></span>

<span data-ttu-id="a233c-122">Het volgende is een voor bereiding van een REGI ster van qubits in een verwerkings status die wordt vertegenwoordigd door een klassieke-bits teken reeks, gegeven als een matrix met `Bool` waarden:</span><span class="sxs-lookup"><span data-stu-id="a233c-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="a233c-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a233c-123">See Also</span></span>

- [<span data-ttu-id="a233c-124">Micro soft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="a233c-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="a233c-125">Micro soft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="a233c-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="a233c-126">Micro soft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="a233c-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)