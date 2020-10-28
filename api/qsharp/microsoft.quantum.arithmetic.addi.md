---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Bewerking AddI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 7ee2b9099ea65b95647422dadc1efe4bf043d147
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707653"
---
# <a name="addi-operation"></a><span data-ttu-id="ff81c-102">Bewerking AddI</span><span class="sxs-lookup"><span data-stu-id="ff81c-102">AddI operation</span></span>

<span data-ttu-id="ff81c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ff81c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ff81c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ff81c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ff81c-105">Automatisch gekozen tussen toevoeging en zonder, afhankelijk van de kassa grootte van `ys` .</span><span class="sxs-lookup"><span data-stu-id="ff81c-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ff81c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ff81c-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="ff81c-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ff81c-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ff81c-108">$n $-bits optelling.</span><span class="sxs-lookup"><span data-stu-id="ff81c-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="ff81c-109">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ff81c-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ff81c-110">Optelling met ten minste $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="ff81c-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="ff81c-111">Het resultaat wordt bewaard.</span><span class="sxs-lookup"><span data-stu-id="ff81c-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ff81c-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ff81c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

