---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Bewerking MultiplyAndAddByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706404"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="0b6b5-102">Bewerking MultiplyAndAddByModularInteger</span><span class="sxs-lookup"><span data-stu-id="0b6b5-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="0b6b5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0b6b5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0b6b5-105">Voert een modulaire vermenigvuldiging en toevoegen door gehele getallen in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="0b6b5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0b6b5-106">Description</span></span>

<span data-ttu-id="0b6b5-107">Implementeert de kaart $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $ $ voor een gegeven modulus $N $, constante multiplier $a $ en summand $y $.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="0b6b5-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="0b6b5-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="0b6b5-109">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0b6b5-110">Een geheel getal $a $ dat moet worden toegevoegd aan elk basis status label.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="0b6b5-111">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0b6b5-112">De modulus $N $ die optellen en vermenigvuldigen met betrekking tot.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="0b6b5-113">vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0b6b5-114">Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt waarvan de waarde moet worden toegevoegd aan elk basis status label van `summand` .</span><span class="sxs-lookup"><span data-stu-id="0b6b5-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="0b6b5-115">summand: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0b6b5-116">Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt dat moet worden gebruikt als doel voor deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0b6b5-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0b6b5-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0b6b5-118">Remarks</span></span>

- <span data-ttu-id="0b6b5-119">Zie afbeelding 6 op [pagina 7 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7) voor het circuit diagram en de uitleg.</span><span class="sxs-lookup"><span data-stu-id="0b6b5-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="0b6b5-120">Deze bewerking komt overeen met CMULT (a) MOD (N) in [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="0b6b5-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="0b6b5-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0b6b5-121">See Also</span></span>

- [<span data-ttu-id="0b6b5-122">Micro soft. Quantum. aritmetische. MultiplyAndAddPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="0b6b5-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)