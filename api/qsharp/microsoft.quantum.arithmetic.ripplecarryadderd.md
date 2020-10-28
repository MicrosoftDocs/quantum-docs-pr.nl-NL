---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderD
title: Bewerking RippleCarryAdderD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderD
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: c4466feebb8ff6afcdcb5bf385ec10e807c00537
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706253"
---
# <a name="ripplecarryadderd-operation"></a><span data-ttu-id="d3816-102">Bewerking RippleCarryAdderD</span><span class="sxs-lookup"><span data-stu-id="d3816-102">RippleCarryAdderD operation</span></span>

<span data-ttu-id="d3816-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d3816-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d3816-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3816-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3816-105">Omkeerbaar, in-place rimpels, toevoeging van twee gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="d3816-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="d3816-106">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , en een Qubit-overdracht, berekent de bewerking de som van de twee gehele getallen waarbij de $n $ minst significante bits van het resultaat worden vastgehouden in en de verwerkings- `ys` bit is xored aan de Qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="d3816-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderD (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d3816-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="d3816-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="d3816-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d3816-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d3816-109">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="d3816-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="d3816-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d3816-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d3816-111">LittleEndian Qubit registreren code ring de tweede integer summand is gewijzigd in de $n $ minst significante bits van de som.</span><span class="sxs-lookup"><span data-stu-id="d3816-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="d3816-112">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d3816-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d3816-113">Qubit, is xored met de meest significante bit van de som.</span><span class="sxs-lookup"><span data-stu-id="d3816-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3816-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3816-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d3816-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d3816-115">Remarks</span></span>

<span data-ttu-id="d3816-116">De opgegeven bewaakte bewerking maakt gebruik van symmetrie en wederzijdse annulering van bewerkingen voor het verbeteren van de standaard implementatie waarmee een besturings element wordt toegevoegd aan elke bewerking.</span><span class="sxs-lookup"><span data-stu-id="d3816-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="d3816-117">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="d3816-117">References</span></span>

- <span data-ttu-id="d3816-118">Thomas G. Draper: "toevoegen op een quantum computer", 2000.</span><span class="sxs-lookup"><span data-stu-id="d3816-118">Thomas G. Draper: "Addition on a Quantum Computer", 2000.</span></span>
  https://arxiv.org/abs/quant-ph/0008033