---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Bewerking AddI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843851"
---
# <a name="addi-operation"></a><span data-ttu-id="24260-102">Bewerking AddI</span><span class="sxs-lookup"><span data-stu-id="24260-102">AddI operation</span></span>

<span data-ttu-id="24260-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="24260-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="24260-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="24260-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="24260-105">Automatisch gekozen tussen toevoeging en zonder, afhankelijk van de kassa grootte van `ys` .</span><span class="sxs-lookup"><span data-stu-id="24260-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="24260-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="24260-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="24260-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="24260-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="24260-108">$n $-bits optelling.</span><span class="sxs-lookup"><span data-stu-id="24260-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="24260-109">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="24260-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="24260-110">Optelling met ten minste $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="24260-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="24260-111">Het resultaat wordt bewaard.</span><span class="sxs-lookup"><span data-stu-id="24260-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="24260-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="24260-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

