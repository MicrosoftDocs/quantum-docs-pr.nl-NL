---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Bewerking RippleCarryAdderCDKM
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: 6dcb5193c5d1d059682a79e63e6562aabff7539d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706269"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="3447a-102">Bewerking RippleCarryAdderCDKM</span><span class="sxs-lookup"><span data-stu-id="3447a-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="3447a-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3447a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3447a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3447a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3447a-105">Omkeerbaar, in-place rimpels, toevoeging van twee gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="3447a-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="3447a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3447a-106">Description</span></span>

<span data-ttu-id="3447a-107">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , en een Qubit-overdracht, berekent de bewerking de som van de twee gehele getallen waarbij de $n $ minst significante bits van het resultaat worden vastgehouden in en de verwerkings- `ys` bit is xored aan de Qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="3447a-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="3447a-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="3447a-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="3447a-109">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3447a-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3447a-110">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="3447a-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="3447a-111">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3447a-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3447a-112">LittleEndian Qubit registreren code ring de tweede integer summand, wordt aangepast om de n minst significante bits van de som op te slaan.</span><span class="sxs-lookup"><span data-stu-id="3447a-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="3447a-113">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3447a-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3447a-114">Qubit, is xored met de meest significante bit van de som.</span><span class="sxs-lookup"><span data-stu-id="3447a-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3447a-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3447a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3447a-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3447a-116">Remarks</span></span>

<span data-ttu-id="3447a-117">Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderD, maar gebruikt slechts één hulp Qubit in plaats van $n $.</span><span class="sxs-lookup"><span data-stu-id="3447a-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="3447a-118">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="3447a-118">References</span></span>

- <span data-ttu-id="3447a-119">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="3447a-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1