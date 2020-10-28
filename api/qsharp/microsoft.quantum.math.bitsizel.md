---
uid: Microsoft.Quantum.Math.BitSizeL
title: De functie BitSizeL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 97068f12050317a9aa17c95f33650ef6f406066d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708304"
---
# <a name="bitsizel-function"></a><span data-ttu-id="95613-102">De functie BitSizeL</span><span class="sxs-lookup"><span data-stu-id="95613-102">BitSizeL function</span></span>

<span data-ttu-id="95613-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="95613-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="95613-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="95613-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="95613-105">Voor een niet-negatief geheel getal `a` retourneert het aantal bits dat is vereist om aan te duiden `a` .</span><span class="sxs-lookup"><span data-stu-id="95613-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="95613-106">Dat wil zeggen, retourneert de kleinste $n $, zodat $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="95613-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="95613-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="95613-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="95613-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="95613-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="95613-109">Het gehele getal waarvan de bitlengte moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="95613-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="95613-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="95613-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="95613-111">De bits-grootte van `a` .</span><span class="sxs-lookup"><span data-stu-id="95613-111">The bit-size of `a`.</span></span>