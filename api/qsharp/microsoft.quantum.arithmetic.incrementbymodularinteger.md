---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Bewerking IncrementByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: f5bacef299ab0b3627e757abdcaa798cf9b2e7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846607"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="d17f2-102">Bewerking IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="d17f2-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="d17f2-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d17f2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d17f2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d17f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d17f2-105">Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="d17f2-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d17f2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d17f2-106">Description</span></span>

<span data-ttu-id="d17f2-107">Laat het ons weten door `increment` $a $ `modulus` door $N $ en een geheel getal dat is gecodeerd in `target` $y $.</span><span class="sxs-lookup"><span data-stu-id="d17f2-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="d17f2-108">De bewerking voert vervolgens de volgende trans formatie uit: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} gehele getallen worden gecodeerd in de indeling little-endian.</span><span class="sxs-lookup"><span data-stu-id="d17f2-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="d17f2-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="d17f2-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="d17f2-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d17f2-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d17f2-111">Geheel getal $a $ dat moet worden toegevoegd aan $y $.</span><span class="sxs-lookup"><span data-stu-id="d17f2-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="d17f2-112">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d17f2-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d17f2-113">Geheel getal $N $ dat modules $y + a $.</span><span class="sxs-lookup"><span data-stu-id="d17f2-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="d17f2-114">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d17f2-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d17f2-115">Geheel getal $y $ in `LittleEndian` indeling waaraan `increment` $a $ is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d17f2-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d17f2-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d17f2-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d17f2-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d17f2-117">Remarks</span></span>

<span data-ttu-id="d17f2-118">Er wordt van uitgegaan dat de aanvankelijke waarde van target kleiner is dan $N $ en dat de verhoging $a $ kleiner is dan $N $.</span><span class="sxs-lookup"><span data-stu-id="d17f2-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="d17f2-119">Houd er rekening mee dat <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> dezelfde bewerking in de `PhaseLittleEndian` basis wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="d17f2-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="d17f2-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d17f2-120">See Also</span></span>

- [<span data-ttu-id="d17f2-121">Micro soft. Quantum. aritmetische. IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="d17f2-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)