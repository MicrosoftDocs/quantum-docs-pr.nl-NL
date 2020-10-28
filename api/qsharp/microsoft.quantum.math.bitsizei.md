---
uid: Microsoft.Quantum.Math.BitSizeI
title: De functie BitSizeI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7cfe03908a8a394fc8ceb1c9facbf02f3db2d48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708305"
---
# <a name="bitsizei-function"></a><span data-ttu-id="8be59-102">De functie BitSizeI</span><span class="sxs-lookup"><span data-stu-id="8be59-102">BitSizeI function</span></span>

<span data-ttu-id="8be59-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8be59-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8be59-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8be59-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8be59-105">Voor een niet-negatief geheel getal `a` retourneert het aantal bits dat is vereist om aan te duiden `a` .</span><span class="sxs-lookup"><span data-stu-id="8be59-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="8be59-106">Dat wil zeggen, retourneert de kleinste $n $, zodat $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="8be59-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="8be59-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="8be59-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="8be59-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8be59-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8be59-109">Het gehele getal waarvan de bitlengte moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="8be59-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="8be59-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8be59-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8be59-111">De bits-grootte van `a` .</span><span class="sxs-lookup"><span data-stu-id="8be59-111">The bit-size of `a`.</span></span>