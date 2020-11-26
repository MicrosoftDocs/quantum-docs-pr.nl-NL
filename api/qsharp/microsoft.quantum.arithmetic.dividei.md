---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Bewerking DivideI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 4cff191e1f9d42659768b4059e477f1a07948ba1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223303"
---
# <a name="dividei-operation"></a><span data-ttu-id="0a00a-102">Bewerking DivideI</span><span class="sxs-lookup"><span data-stu-id="0a00a-102">DivideI operation</span></span>

<span data-ttu-id="0a00a-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0a00a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0a00a-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0a00a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0a00a-105">Deelt twee Quantum-gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="0a00a-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="0a00a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0a00a-106">Description</span></span>

<span data-ttu-id="0a00a-107">`xs` houdt het restant `xs - floor(xs/ys) * ys` en `result` zal in beslaan `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="0a00a-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="0a00a-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="0a00a-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="0a00a-109">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a00a-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a00a-110">$n $-bits-dividend wordt vervangen door de rest.</span><span class="sxs-lookup"><span data-stu-id="0a00a-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="0a00a-111">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a00a-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a00a-112">$-bit-deler $n</span><span class="sxs-lookup"><span data-stu-id="0a00a-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="0a00a-113">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a00a-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a00a-114">$n $-bit-resultaat moet de status $ \ket {0} $ in eerste instantie hebben en wordt vervangen door het resultaat van de deling geheel getal.</span><span class="sxs-lookup"><span data-stu-id="0a00a-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a00a-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a00a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0a00a-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0a00a-116">Remarks</span></span>

<span data-ttu-id="0a00a-117">Maakt gebruik van een standaard aanpak voor Shift en aftrekken om de deling te implementeren.</span><span class="sxs-lookup"><span data-stu-id="0a00a-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="0a00a-118">De gecontroleerde versie is gespecialiseerd, maar er zijn geen extra besturings elementen vereist voor het aftrekken.</span><span class="sxs-lookup"><span data-stu-id="0a00a-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>