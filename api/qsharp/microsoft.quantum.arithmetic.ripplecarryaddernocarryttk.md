---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Bewerking RippleCarryAdderNoCarryTTK
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: a539d85a4800c2f4452a1c6fe2c4f88a6296c3e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221994"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="c6de8-102">Bewerking RippleCarryAdderNoCarryTTK</span><span class="sxs-lookup"><span data-stu-id="c6de8-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="c6de8-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c6de8-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c6de8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c6de8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c6de8-105">Omkeerbaar, in-place rimpels, waarbij twee gehele getallen worden toegevoegd zonder dat ze worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c6de8-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c6de8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c6de8-106">Description</span></span>

<span data-ttu-id="c6de8-107">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , berekent de bewerking de som van de twee gehele getallen modulo $2 ^ n $, waarbij $n $ de bitlengte is van de invoer `xs` en `ys` .</span><span class="sxs-lookup"><span data-stu-id="c6de8-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="c6de8-108">De verwerkings bit wordt niet berekend.</span><span class="sxs-lookup"><span data-stu-id="c6de8-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="c6de8-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="c6de8-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="c6de8-110">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c6de8-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c6de8-111">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="c6de8-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="c6de8-112">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c6de8-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c6de8-113">LittleEndian Qubit registreren code ring de tweede integer summand is gewijzigd in de $n $ minst significante bits van de som.</span><span class="sxs-lookup"><span data-stu-id="c6de8-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c6de8-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c6de8-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6de8-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c6de8-115">Remarks</span></span>

<span data-ttu-id="c6de8-116">Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderTTK, maar retourneert niet de draag bit.</span><span class="sxs-lookup"><span data-stu-id="c6de8-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="c6de8-117">Referenties</span><span class="sxs-lookup"><span data-stu-id="c6de8-117">References</span></span>

- <span data-ttu-id="c6de8-118">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="c6de8-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530