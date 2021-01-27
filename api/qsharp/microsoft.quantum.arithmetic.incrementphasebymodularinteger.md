---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Bewerking IncrementPhaseByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 4ba35010d56ad01c73cb563646dc8150842da12e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846581"
---
# <a name="incrementphasebymodularinteger-operation"></a><span data-ttu-id="44e43-102">Bewerking IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="44e43-102">IncrementPhaseByModularInteger operation</span></span>

<span data-ttu-id="44e43-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="44e43-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="44e43-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="44e43-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="44e43-105">Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="44e43-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="44e43-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="44e43-106">Description</span></span>

<span data-ttu-id="44e43-107">Laat het ons weten door `increment` $a $ `modulus` door $N $ en een geheel getal dat is gecodeerd in `target` $y $.</span><span class="sxs-lookup"><span data-stu-id="44e43-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="44e43-108">De bewerking voert vervolgens de volgende trans formatie uit: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} gehele getallen worden in QFT gebaseerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="44e43-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format in QFT basis.</span></span>

## <a name="input"></a><span data-ttu-id="44e43-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="44e43-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="44e43-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="44e43-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="44e43-111">Geheel getal $a $ dat moet worden toegevoegd aan $y $.</span><span class="sxs-lookup"><span data-stu-id="44e43-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="44e43-112">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="44e43-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="44e43-113">Geheel getal $N $ dat modules $y + a $.</span><span class="sxs-lookup"><span data-stu-id="44e43-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="44e43-114">doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="44e43-114">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="44e43-115">Geheel getal $y $ in een indeling die uit een Phase-code is versleuteld `increment` en waaraan $a $ is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="44e43-115">Integer $y$ in phase-encoded little-endian format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="44e43-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="44e43-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="44e43-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="44e43-117">Remarks</span></span>

<span data-ttu-id="44e43-118">Er wordt van uitgegaan dat `target` de hoogste bit is ingesteld op 0.</span><span class="sxs-lookup"><span data-stu-id="44e43-118">Assumes that `target` has the highest bit set to 0.</span></span>
<span data-ttu-id="44e43-119">Er wordt ook van uitgegaan dat de waarde van target kleiner is dan $N $.</span><span class="sxs-lookup"><span data-stu-id="44e43-119">Also assumes that the value of target is less than $N$.</span></span>

<span data-ttu-id="44e43-120">Zie afbeelding 5 op [pagina 5 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5)voor het circuit diagram en de uitleg.</span><span class="sxs-lookup"><span data-stu-id="44e43-120">For the circuit diagram and explanation see Figure 5 on [Page 5 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span></span>

## <a name="see-also"></a><span data-ttu-id="44e43-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="44e43-121">See Also</span></span>

- [<span data-ttu-id="44e43-122">Micro soft. Quantum. aritmetische. IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="44e43-122">Microsoft.Quantum.Arithmetic.IncrementByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)