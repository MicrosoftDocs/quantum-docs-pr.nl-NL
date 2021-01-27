---
uid: Microsoft.Quantum.Math.BitSizeI
title: De functie BitSizeI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7edf37a81571dfa1d4cb755493e1863a44c694e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857701"
---
# <a name="bitsizei-function"></a><span data-ttu-id="abe7a-102">De functie BitSizeI</span><span class="sxs-lookup"><span data-stu-id="abe7a-102">BitSizeI function</span></span>

<span data-ttu-id="abe7a-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="abe7a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="abe7a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="abe7a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="abe7a-105">Voor een niet-negatief geheel getal `a` retourneert het aantal bits dat is vereist om aan te duiden `a` .</span><span class="sxs-lookup"><span data-stu-id="abe7a-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="abe7a-106">Dat wil zeggen, retourneert de kleinste $n $, zodat $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="abe7a-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="abe7a-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="abe7a-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="abe7a-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="abe7a-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="abe7a-109">Het gehele getal waarvan de bitlengte moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="abe7a-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="abe7a-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="abe7a-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="abe7a-111">De bits-grootte van `a` .</span><span class="sxs-lookup"><span data-stu-id="abe7a-111">The bit-size of `a`.</span></span>