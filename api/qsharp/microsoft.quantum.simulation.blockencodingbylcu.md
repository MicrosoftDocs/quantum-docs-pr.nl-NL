---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: De functie BlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 04738aa54ce8b719b05954824e3553388a995df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709019"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="6db36-102">De functie BlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="6db36-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="6db36-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6db36-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6db36-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6db36-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6db36-105">Codeert een operator van belang in een `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="6db36-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="6db36-106">Hiermee wordt een `BlockEncoding` unitary $U = P\cdot V\cdot P ^ \dagger $ waarmee een bepaalde operator wordt gecodeerd $H = \ sum_ {j} | \ alpha_j | U_j $ van belang dat een lineaire combi natie is van unitaries.</span><span class="sxs-lookup"><span data-stu-id="6db36-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="6db36-107">Normaal gesp roken is $P $ een status voorbereiding unitary, zodat $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ en $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="6db36-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="6db36-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6db36-108">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="6db36-109">statePreparation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="6db36-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="6db36-110">Een unitary $P $ die een bepaalde doel status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="6db36-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="6db36-111">kiezer: ('T) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="6db36-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="6db36-112">Een unitary $V $ waarmee het onderdeel unitaries van $H $ wordt gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="6db36-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit-adj--ctl"></a><span data-ttu-id="6db36-113">Output: ('T) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="6db36-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="6db36-114">Een unitary $U $ communiceert gezamenlijk aan registers `a` en `s` die blok-coderingen $H $, en voldoet aan $U ^ \Dagger = U $.</span><span class="sxs-lookup"><span data-stu-id="6db36-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6db36-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6db36-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6db36-116">T</span><span class="sxs-lookup"><span data-stu-id="6db36-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="6db36-117">Maatschappij</span><span class="sxs-lookup"><span data-stu-id="6db36-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="6db36-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6db36-118">Remarks</span></span>

<span data-ttu-id="6db36-119">Deze `BlockEncoding` implementatie geeft de eigenschappen van een `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="6db36-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6db36-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6db36-120">See Also</span></span>

- [<span data-ttu-id="6db36-121">Micro soft. Quantum. simulatie. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="6db36-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="6db36-122">Micro soft. Quantum. simulatie. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="6db36-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)