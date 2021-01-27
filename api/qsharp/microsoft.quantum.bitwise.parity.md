---
uid: Microsoft.Quantum.Bitwise.Parity
title: De functie parity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Parity
qsharp.summary: Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).
ms.openlocfilehash: b34ef36b0336ec1dea7fdbd878c6d695b38d623e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842128"
---
# <a name="parity-function"></a><span data-ttu-id="ff61d-102">De functie parity</span><span class="sxs-lookup"><span data-stu-id="ff61d-102">Parity function</span></span>

<span data-ttu-id="ff61d-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="ff61d-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="ff61d-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ff61d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ff61d-105">Retourneert de bitsgewijze PARITEIT van een geheel getal (1 als de binaire representatie een oneven aantal records bevat en 0 anders).</span><span class="sxs-lookup"><span data-stu-id="ff61d-105">Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).</span></span>

```qsharp
function Parity (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="ff61d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ff61d-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ff61d-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ff61d-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="ff61d-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ff61d-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="ff61d-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ff61d-109">Example</span></span>

```qsharp
let a = 248;
let x = Parity(a); // x : Int = 1.
```