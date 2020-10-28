---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Bewerking IncrementByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707261"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="dcaa9-102">Bewerking IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="dcaa9-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="dcaa9-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dcaa9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dcaa9-105">Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="dcaa9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dcaa9-106">Description</span></span>

<span data-ttu-id="dcaa9-107">Laat het ons weten door `increment` $a $ `modulus` door $N $ en een geheel getal dat is gecodeerd in `target` $y $.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="dcaa9-108">De bewerking voert vervolgens de volgende trans formatie uit: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} gehele getallen worden gecodeerd in de indeling little-endian.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="dcaa9-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="dcaa9-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="dcaa9-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dcaa9-111">Geheel getal $a $ dat moet worden toegevoegd aan $y $.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="dcaa9-112">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dcaa9-113">Geheel getal $N $ dat modules $y + a $.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="dcaa9-114">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dcaa9-115">Geheel getal $y $ in `LittleEndian` indeling waaraan `increment` $a $ is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dcaa9-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dcaa9-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dcaa9-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dcaa9-117">Remarks</span></span>

<span data-ttu-id="dcaa9-118">Er wordt van uitgegaan dat de aanvankelijke waarde van target kleiner is dan $N $ en dat de verhoging $a $ kleiner is dan $N $.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="dcaa9-119">Houd er rekening mee dat <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> dezelfde bewerking in de `PhaseLittleEndian` basis wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="dcaa9-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcaa9-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dcaa9-120">See Also</span></span>

- [<span data-ttu-id="dcaa9-121">Micro soft. Quantum. aritmetische. IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="dcaa9-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)