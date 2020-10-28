---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Bewerking SquareI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: d7334d50f245ba358624e6e2eee94b63d9ed7569
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706221"
---
# <a name="squarei-operation"></a><span data-ttu-id="ac60d-102">Bewerking SquareI</span><span class="sxs-lookup"><span data-stu-id="ac60d-102">SquareI operation</span></span>

<span data-ttu-id="ac60d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ac60d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ac60d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ac60d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ac60d-105">Berekent het kwadraat van het gehele getal `xs` in `result` , die in eerste instantie nul moet zijn.</span><span class="sxs-lookup"><span data-stu-id="ac60d-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ac60d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ac60d-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="ac60d-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac60d-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ac60d-108">$n $-bits nummer naar vier kant (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac60d-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="ac60d-109">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac60d-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ac60d-110">$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="ac60d-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ac60d-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac60d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ac60d-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ac60d-112">Remarks</span></span>

<span data-ttu-id="ac60d-113">Maakt gebruik van een standaard methode voor Shift en toevoegen om het kwadraat te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ac60d-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="ac60d-114">Slaat $n-$1 qubits op vergeleken met de oplossing voor rechtse, die eerst XS kopieert voordat een gewone vermenigvuldiger wordt toegepast en vervolgens de Kopieer bewerking ongedaan wordt.</span><span class="sxs-lookup"><span data-stu-id="ac60d-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>