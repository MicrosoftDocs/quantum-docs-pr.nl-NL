---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: De functie BlockEncodingByLCU
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 254ace01750f94e6c871de9b62f1342000bc84ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229542"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="667bd-102">De functie BlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="667bd-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="667bd-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="667bd-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="667bd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="667bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="667bd-105">Codeert een operator van belang in een `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="667bd-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="667bd-106">Hiermee wordt een `BlockEncoding` unitary $U = P\cdot V\cdot P ^ \dagger $ waarmee een bepaalde operator wordt gecodeerd $H = \ sum_ {j} | \ alpha_j | U_j $ van belang dat een lineaire combi natie is van unitaries.</span><span class="sxs-lookup"><span data-stu-id="667bd-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="667bd-107">Normaal gesp roken is $P $ een status voorbereiding unitary, zodat $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ en $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="667bd-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="667bd-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="667bd-108">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="667bd-109">statePreparation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="667bd-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="667bd-110">Een unitary $P $ die een bepaalde doel status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="667bd-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="667bd-111">kiezer: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="667bd-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="667bd-112">Een unitary $V $ waarmee het onderdeel unitaries van $H $ wordt gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="667bd-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit--is-adj--ctl"></a><span data-ttu-id="667bd-113">Output: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="667bd-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="667bd-114">Een unitary $U $ communiceert gezamenlijk aan registers `a` en `s` die blok-coderingen $H $, en voldoet aan $U ^ \Dagger = U $.</span><span class="sxs-lookup"><span data-stu-id="667bd-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="667bd-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="667bd-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="667bd-116">T</span><span class="sxs-lookup"><span data-stu-id="667bd-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="667bd-117">Maatschappij</span><span class="sxs-lookup"><span data-stu-id="667bd-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="667bd-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="667bd-118">Remarks</span></span>

<span data-ttu-id="667bd-119">Deze `BlockEncoding` implementatie geeft de eigenschappen van een `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="667bd-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="667bd-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="667bd-120">See Also</span></span>

- [<span data-ttu-id="667bd-121">Micro soft. Quantum. simulatie. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="667bd-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="667bd-122">Micro soft. Quantum. simulatie. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="667bd-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)