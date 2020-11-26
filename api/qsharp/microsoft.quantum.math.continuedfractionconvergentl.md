---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: De functie ContinuedFractionConvergentL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c10fcbbe63d3d4c7d6c56196768c1062be1ca350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210927"
---
# <a name="continuedfractionconvergentl-function"></a><span data-ttu-id="38eab-102">De functie ContinuedFractionConvergentL</span><span class="sxs-lookup"><span data-stu-id="38eab-102">ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="38eab-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="38eab-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="38eab-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="38eab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="38eab-105">Hiermee wordt gezocht naar de voortgezette fractie convergent die het dichtst bij `fraction` met de noemer kleiner of gelijk is aan `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="38eab-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="38eab-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="38eab-106">Input</span></span>

### <a name="fraction--bigfraction"></a><span data-ttu-id="38eab-107">Fractie: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="38eab-107">fraction : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="38eab-108">denominatorBound: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="38eab-108">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="38eab-109">Uitvoer: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="38eab-109">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

<span data-ttu-id="38eab-110">Achterliggende fractie die het dichtst bij `fraction` met de noemer kleiner of gelijk aan `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="38eab-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>