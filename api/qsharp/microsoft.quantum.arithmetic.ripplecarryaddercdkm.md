---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Bewerking RippleCarryAdderCDKM
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: df9b62b649af532a4202aacc3e8dd4613eb8665d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846365"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="e136b-102">Bewerking RippleCarryAdderCDKM</span><span class="sxs-lookup"><span data-stu-id="e136b-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="e136b-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e136b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e136b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e136b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e136b-105">Omkeerbaar, in-place rimpels, toevoeging van twee gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="e136b-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e136b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e136b-106">Description</span></span>

<span data-ttu-id="e136b-107">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , en een Qubit-overdracht, berekent de bewerking de som van de twee gehele getallen waarbij de $n $ minst significante bits van het resultaat worden vastgehouden in en de verwerkings- `ys` bit is xored aan de Qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="e136b-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="e136b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e136b-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e136b-109">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e136b-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e136b-110">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="e136b-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="e136b-111">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e136b-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e136b-112">LittleEndian Qubit registreren code ring de tweede integer summand, wordt aangepast om de n minst significante bits van de som op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e136b-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="e136b-113">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e136b-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e136b-114">Qubit, is xored met de meest significante bit van de som.</span><span class="sxs-lookup"><span data-stu-id="e136b-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e136b-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e136b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e136b-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e136b-116">Remarks</span></span>

<span data-ttu-id="e136b-117">Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderD, maar gebruikt slechts één hulp Qubit in plaats van $n $.</span><span class="sxs-lookup"><span data-stu-id="e136b-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="e136b-118">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="e136b-118">References</span></span>

- <span data-ttu-id="e136b-119">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="e136b-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1