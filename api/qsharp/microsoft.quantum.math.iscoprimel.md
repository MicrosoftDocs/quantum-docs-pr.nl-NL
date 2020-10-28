---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: De functie IsCoprimeL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 7c077d508c93672d58a52a1403b3c5d73df75471
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707926"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="ee1c6-102">De functie IsCoprimeL</span><span class="sxs-lookup"><span data-stu-id="ee1c6-102">IsCoprimeL function</span></span>

<span data-ttu-id="ee1c6-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ee1c6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ee1c6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ee1c6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ee1c6-105">Retourneert waar als $a $ en $b $ co-Prime en ONWAAR anders zijn.</span><span class="sxs-lookup"><span data-stu-id="ee1c6-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="ee1c6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ee1c6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="ee1c6-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ee1c6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ee1c6-108">het eerste getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="ee1c6-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="ee1c6-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ee1c6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ee1c6-110">het tweede getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="ee1c6-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="ee1c6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ee1c6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ee1c6-112">Waar, als $a $ en $b $ co-Prime zijn (bijvoorbeeld de grootste gemene deler is 1) en ONWAAR, anders</span><span class="sxs-lookup"><span data-stu-id="ee1c6-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>