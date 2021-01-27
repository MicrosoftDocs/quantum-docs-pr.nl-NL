---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderTTK
title: Bewerking RippleCarryAdderTTK
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: cf7f8ed10de2243627a001b770a4d29ff7345f30
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842949"
---
# <a name="ripplecarryadderttk-operation"></a><span data-ttu-id="c66a5-102">Bewerking RippleCarryAdderTTK</span><span class="sxs-lookup"><span data-stu-id="c66a5-102">RippleCarryAdderTTK operation</span></span>

<span data-ttu-id="c66a5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c66a5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c66a5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c66a5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c66a5-105">Omkeerbaar, in-place rimpels, toevoeging van twee gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="c66a5-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="c66a5-106">Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , en een Qubit-overdracht, berekent de bewerking de som van de twee gehele getallen waarbij de $n $ minst significante bits van het resultaat worden vastgehouden in en de verwerkings- `ys` bit is xored aan de Qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="c66a5-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c66a5-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c66a5-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="c66a5-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c66a5-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c66a5-109">LittleEndian Qubit registreert de eerste integer summand.</span><span class="sxs-lookup"><span data-stu-id="c66a5-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="c66a5-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c66a5-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c66a5-111">LittleEndian Qubit registreren code ring de tweede integer summand is gewijzigd in de $n $ minst significante bits van de som.</span><span class="sxs-lookup"><span data-stu-id="c66a5-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="c66a5-112">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c66a5-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c66a5-113">Qubit, is xored met de meest significante bit van de som.</span><span class="sxs-lookup"><span data-stu-id="c66a5-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c66a5-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c66a5-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c66a5-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c66a5-115">Remarks</span></span>

<span data-ttu-id="c66a5-116">Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderD en RippleCarryAdderCDKM, maar gebruikt geen ancilla qubits.</span><span class="sxs-lookup"><span data-stu-id="c66a5-116">This operation has the same functionality as RippleCarryAdderD and, RippleCarryAdderCDKM but does not use any ancilla qubits.</span></span>

## <a name="references"></a><span data-ttu-id="c66a5-117">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="c66a5-117">References</span></span>

- <span data-ttu-id="c66a5-118">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="c66a5-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530