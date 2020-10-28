---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: De functie IsCoprimeI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: bdfaecb61f56967e21bf85ba190638b43685214d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708376"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="4171c-102">De functie IsCoprimeI</span><span class="sxs-lookup"><span data-stu-id="4171c-102">IsCoprimeI function</span></span>

<span data-ttu-id="4171c-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4171c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4171c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4171c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4171c-105">Retourneert waar als $a $ en $b $ co-Prime en ONWAAR anders zijn.</span><span class="sxs-lookup"><span data-stu-id="4171c-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="4171c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4171c-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="4171c-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4171c-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4171c-108">het eerste getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="4171c-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="4171c-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4171c-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4171c-110">het tweede getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="4171c-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="4171c-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4171c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4171c-112">Waar, als $a $ en $b $ co-Prime zijn (bijvoorbeeld de grootste gemene deler is 1) en ONWAAR, anders</span><span class="sxs-lookup"><span data-stu-id="4171c-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>