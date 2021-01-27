---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Bewerking DivideI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846689"
---
# <a name="dividei-operation"></a><span data-ttu-id="4b404-102">Bewerking DivideI</span><span class="sxs-lookup"><span data-stu-id="4b404-102">DivideI operation</span></span>

<span data-ttu-id="4b404-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4b404-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4b404-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="4b404-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="4b404-105">Deelt twee Quantum-gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="4b404-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4b404-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4b404-106">Description</span></span>

<span data-ttu-id="4b404-107">`xs` houdt het restant `xs - floor(xs/ys) * ys` en `result` zal in beslaan `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="4b404-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="4b404-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4b404-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="4b404-109">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4b404-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4b404-110">$n $-bits-dividend wordt vervangen door de rest.</span><span class="sxs-lookup"><span data-stu-id="4b404-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="4b404-111">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4b404-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4b404-112">$-bit-deler $n</span><span class="sxs-lookup"><span data-stu-id="4b404-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="4b404-113">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4b404-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4b404-114">$n $-bit-resultaat moet de status $ \ket {0} $ in eerste instantie hebben en wordt vervangen door het resultaat van de deling geheel getal.</span><span class="sxs-lookup"><span data-stu-id="4b404-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4b404-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4b404-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4b404-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4b404-116">Remarks</span></span>

<span data-ttu-id="4b404-117">Maakt gebruik van een standaard aanpak voor Shift en aftrekken om de deling te implementeren.</span><span class="sxs-lookup"><span data-stu-id="4b404-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="4b404-118">De gecontroleerde versie is gespecialiseerd, maar er zijn geen extra besturings elementen vereist voor het aftrekken.</span><span class="sxs-lookup"><span data-stu-id="4b404-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>