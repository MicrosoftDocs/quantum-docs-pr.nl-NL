---
uid: Microsoft.Quantum.Math.SquaredNorm
title: De functie SquaredNorm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709090"
---
# <a name="squarednorm-function"></a><span data-ttu-id="e92b7-102">De functie SquaredNorm</span><span class="sxs-lookup"><span data-stu-id="e92b7-102">SquaredNorm function</span></span>

<span data-ttu-id="e92b7-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e92b7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e92b7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e92b7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e92b7-105">Retourneert de vier Kante 2-norm van een vector.</span><span class="sxs-lookup"><span data-stu-id="e92b7-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="e92b7-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e92b7-106">Description</span></span>

<span data-ttu-id="e92b7-107">Retourneert de vier Kante 2-norm van een vector; op basis van de invoer $ \vec{x} $ retourneert $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="e92b7-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="e92b7-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e92b7-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="e92b7-109">matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e92b7-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e92b7-110">De vector waarvan het kwadraat 2-norm moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e92b7-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="e92b7-111">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e92b7-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e92b7-112">De vier Kante 2-norm van `array` .</span><span class="sxs-lookup"><span data-stu-id="e92b7-112">The squared 2-norm of `array`.</span></span>