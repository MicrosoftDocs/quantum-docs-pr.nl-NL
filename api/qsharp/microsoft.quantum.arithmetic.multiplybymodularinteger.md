---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Bewerking MultiplyByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 080414d208a2a0c114857db8e93efb4cd74a4d8d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222572"
---
# <a name="multiplybymodularinteger-operation"></a><span data-ttu-id="5d8c0-102">Bewerking MultiplyByModularInteger</span><span class="sxs-lookup"><span data-stu-id="5d8c0-102">MultiplyByModularInteger operation</span></span>

<span data-ttu-id="5d8c0-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5d8c0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d8c0-105">Voert modulaire vermenigvuldiging uit met een gehele constante in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-105">Performs modular multiplication by an integer constant on a qubit register.</span></span>

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5d8c0-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5d8c0-106">Description</span></span>

<span data-ttu-id="5d8c0-107">Laat het ons weten `modulus` door $N $ en `constMultiplier` door $a $.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-107">Let us denote `modulus` by $N$ and `constMultiplier` by $a$.</span></span>
<span data-ttu-id="5d8c0-108">Met deze bewerking wordt een unitary-bewerking geïmplementeerd die is gedefinieerd door de volgende kaart op basis van de berekening: $ $ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $ $ voor alle $y $ tussen $0 $ en $N-$1.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-108">Then this operation implements a unitary operation defined by the following map on the computational basis: $$ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $$ for all $y$ between $0$ and $N - 1$.</span></span>

## <a name="input"></a><span data-ttu-id="5d8c0-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="5d8c0-109">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="5d8c0-110">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-110">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d8c0-111">De constante waarmee vermenigvuldiger wordt vermenigvuldigd.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-111">Constant by which multiplier is being multiplied.</span></span> <span data-ttu-id="5d8c0-112">Moet een combi natie zijn van de modulus.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-112">Must be co-prime to modulus.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="5d8c0-113">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d8c0-114">De vermenigvuldigings bewerking wordt modulo uitgevoerd `modulus` .</span><span class="sxs-lookup"><span data-stu-id="5d8c0-114">The multiplication operation is performed modulo `modulus`.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="5d8c0-115">vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-115">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5d8c0-116">Het getal dat door een constante wordt vermenigvuldigd.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-116">The number being multiplied by a constant.</span></span>
<span data-ttu-id="5d8c0-117">Dit is een matrix met qubits-code ring: een geheel getal in de indeling little-endian.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-117">This is an array of qubits encoding an integer in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5d8c0-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5d8c0-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5d8c0-119">Remarks</span></span>

- <span data-ttu-id="5d8c0-120">Zie afbeelding 7 op [pagina 8 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8) voor het circuit diagram en de uitleg.</span><span class="sxs-lookup"><span data-stu-id="5d8c0-120">For the circuit diagram and explanation see Figure 7 on [Page 8 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span></span>
- <span data-ttu-id="5d8c0-121">Deze bewerking komt overeen met U ₐ in [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="5d8c0-121">This operation corresponds to Uₐ in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>