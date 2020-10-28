---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Bewerking CarryOutCoreCDKM
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 6a292e66f6d9911d2a9075f6397f4f5ba97ec64d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707397"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="910bb-102">Bewerking CarryOutCoreCDKM</span><span class="sxs-lookup"><span data-stu-id="910bb-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="910bb-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="910bb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="910bb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="910bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="910bb-105">De kern bewerking in de RippleCarryAdderCDKM die wordt gebruikt met de bovenstaande ApplyOuterCDKMAdder-bewerking, dat wil zeggen met deze bewerking, om de binnenste bewerking van de RippleCarryAdderCDKM te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="910bb-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="910bb-106">Met deze bewerking wordt het uitvoeren van Qubit berekend en wordt een reeks van niet-poorten toegepast op een deel van de invoer `ys` .</span><span class="sxs-lookup"><span data-stu-id="910bb-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="910bb-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="910bb-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="910bb-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="910bb-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="910bb-109">Eerste Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="910bb-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="910bb-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="910bb-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="910bb-111">Tweede Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="910bb-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="910bb-112">ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="910bb-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="910bb-113">De ancilla-Qubit die wordt gebruikt in RippleCarryAdderCDKM die is door gegeven aan deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="910bb-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="910bb-114">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="910bb-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="910bb-115">Voer Qubit uit in de RippleCarryAdderCDKM-bewerking.</span><span class="sxs-lookup"><span data-stu-id="910bb-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="910bb-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="910bb-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="910bb-117">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="910bb-117">References</span></span>

- <span data-ttu-id="910bb-118">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="910bb-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1