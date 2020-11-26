---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: De functie BlockEncodingReflectionByLCU
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: e1247d961a7ebce798106c24c46d924dd6e6d347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229474"
---
# <a name="blockencodingreflectionbylcu-function"></a><span data-ttu-id="46ed3-102">De functie BlockEncodingReflectionByLCU</span><span class="sxs-lookup"><span data-stu-id="46ed3-102">BlockEncodingReflectionByLCU function</span></span>

<span data-ttu-id="46ed3-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="46ed3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="46ed3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="46ed3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="46ed3-105">Codeert een operator van belang in een `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="46ed3-105">Encodes an operator of interest into a `BlockEncodingReflection`.</span></span>

<span data-ttu-id="46ed3-106">Hiermee wordt een `BlockEncodingReflection` unitary $U = P\cdot V\cdot P ^ \dagger $ waarmee een bepaalde operator wordt gecodeerd $H = \ sum_ {j} | \ alpha_j | U_j $ van belang dat een lineaire combi natie is van unitaries.</span><span class="sxs-lookup"><span data-stu-id="46ed3-106">This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="46ed3-107">Normaal gesp roken is $P $ een status voorbereidings unitary, zodanig dat $P \ket {0} \_ een \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ en $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="46ed3-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="46ed3-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="46ed3-108">Input</span></span>

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a><span data-ttu-id="46ed3-109">statePreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="46ed3-109">statePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="46ed3-110">Een unitary $P $ die een bepaalde doel status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="46ed3-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="46ed3-111">kiezer: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="46ed3-111">selector : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="46ed3-112">Een unitary $V $ waarmee het onderdeel unitaries van $H $ wordt gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="46ed3-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="46ed3-113">Uitvoer: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="46ed3-113">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="46ed3-114">Een unitary $U $ communiceert gezamenlijk aan registers `a` en `s` die door Block-code ring $H $, en voldoet aan $U ^ {-1} = U $.</span><span class="sxs-lookup"><span data-stu-id="46ed3-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^{-1} = U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ed3-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="46ed3-115">Remarks</span></span>

<span data-ttu-id="46ed3-116">Deze `BlockEncoding` implementatie geeft de eigenschappen van een `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="46ed3-116">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="46ed3-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46ed3-117">See Also</span></span>

- [<span data-ttu-id="46ed3-118">Micro soft. Quantum. simulatie. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="46ed3-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="46ed3-119">Micro soft. Quantum. simulatie. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="46ed3-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)