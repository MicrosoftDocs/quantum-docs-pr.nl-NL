---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Bewerking SquareI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846316"
---
# <a name="squarei-operation"></a><span data-ttu-id="03ee7-102">Bewerking SquareI</span><span class="sxs-lookup"><span data-stu-id="03ee7-102">SquareI operation</span></span>

<span data-ttu-id="03ee7-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="03ee7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="03ee7-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="03ee7-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="03ee7-105">Berekent het kwadraat van het gehele getal `xs` in `result` , die in eerste instantie nul moet zijn.</span><span class="sxs-lookup"><span data-stu-id="03ee7-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="03ee7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="03ee7-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="03ee7-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="03ee7-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="03ee7-108">$n $-bits nummer naar vier kant (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="03ee7-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="03ee7-109">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="03ee7-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="03ee7-110">$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="03ee7-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03ee7-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03ee7-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="03ee7-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="03ee7-112">Remarks</span></span>

<span data-ttu-id="03ee7-113">Maakt gebruik van een standaard methode voor Shift en toevoegen om het kwadraat te berekenen.</span><span class="sxs-lookup"><span data-stu-id="03ee7-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="03ee7-114">Slaat $n-$1 qubits op vergeleken met de oplossing voor rechtse, die eerst XS kopieert voordat een gewone vermenigvuldiger wordt toegepast en vervolgens de Kopieer bewerking ongedaan wordt.</span><span class="sxs-lookup"><span data-stu-id="03ee7-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>