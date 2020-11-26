---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: De functie IdenticalPointPosFactFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223048"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="1376e-102">De functie IdenticalPointPosFactFxP</span><span class="sxs-lookup"><span data-stu-id="1376e-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="1376e-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1376e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1376e-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="1376e-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="1376e-105">U moet bevestigen dat alle vaste-komma getallen in de gegeven matrix identieke punt posities hebben wanneer ze van de minst significante bit worden geteld.</span><span class="sxs-lookup"><span data-stu-id="1376e-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="1376e-106">Dat wil zeggen dat het aantal bits min-punt positie moet constant zijn voor alle vaste-komma getallen in de matrix.</span><span class="sxs-lookup"><span data-stu-id="1376e-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1376e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1376e-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="1376e-108">fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="1376e-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="1376e-109">Matrix van Quantum vaste-komma getallen die worden gecontroleerd op compatibiliteit (met behulp van beweringen).</span><span class="sxs-lookup"><span data-stu-id="1376e-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="1376e-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1376e-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

