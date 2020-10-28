---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: De functie IdenticalPointPosFactFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 0b285ce980ca1abbc3eb20838389a6f49835e742
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707276"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="46899-102">De functie IdenticalPointPosFactFxP</span><span class="sxs-lookup"><span data-stu-id="46899-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="46899-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="46899-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="46899-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46899-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46899-105">U moet bevestigen dat alle vaste-komma getallen in de gegeven matrix identieke punt posities hebben wanneer ze van de minst significante bit worden geteld.</span><span class="sxs-lookup"><span data-stu-id="46899-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="46899-106">Dat wil zeggen dat het aantal bits min-punt positie moet constant zijn voor alle vaste-komma getallen in de matrix.</span><span class="sxs-lookup"><span data-stu-id="46899-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="46899-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="46899-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="46899-108">fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="46899-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="46899-109">Matrix van Quantum vaste-komma getallen die worden gecontroleerd op compatibiliteit (met behulp van beweringen).</span><span class="sxs-lookup"><span data-stu-id="46899-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="46899-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46899-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

