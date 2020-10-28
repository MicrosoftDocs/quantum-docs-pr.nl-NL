---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Bewerking RippleCarryAdderNoCarryTTK
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 59451b4f5c992f900a27139332059af7427b9b93
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706252"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="3ef54-102">Bewerking RippleCarryAdderNoCarryTTK</span><span class="sxs-lookup"><span data-stu-id="3ef54-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="3ef54-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3ef54-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3ef54-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3ef54-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3ef54-105">Omkeerbaar, in-place rimpels, waarbij twee gehele getallen worden toegevoegd zonder dat ze worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3ef54-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="3ef54-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3ef54-106">Description</span></span>

<span data-ttu-id="3ef54-107">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , berekent de bewerking de som van de twee gehele getallen modulo $2 ^ n $, waarbij $n $ de bitlengte is van de invoer `xs` en `ys` .</span><span class="sxs-lookup"><span data-stu-id="3ef54-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="3ef54-108">De verwerkings bit wordt niet berekend.</span><span class="sxs-lookup"><span data-stu-id="3ef54-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="3ef54-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ef54-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="3ef54-110">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ef54-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ef54-111">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="3ef54-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="3ef54-112">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ef54-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ef54-113">LittleEndian Qubit registreren code ring de tweede integer summand is gewijzigd in de $n $ minst significante bits van de som.</span><span class="sxs-lookup"><span data-stu-id="3ef54-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ef54-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ef54-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ef54-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3ef54-115">Remarks</span></span>

<span data-ttu-id="3ef54-116">Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderTTK, maar retourneert niet de draag bit.</span><span class="sxs-lookup"><span data-stu-id="3ef54-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="3ef54-117">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="3ef54-117">References</span></span>

- <span data-ttu-id="3ef54-118">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="3ef54-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530