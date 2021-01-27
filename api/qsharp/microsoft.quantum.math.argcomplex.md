---
uid: Microsoft.Quantum.Math.ArgComplex
title: De functie ArgComplex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842758"
---
# <a name="argcomplex-function"></a><span data-ttu-id="6fe61-102">De functie ArgComplex</span><span class="sxs-lookup"><span data-stu-id="6fe61-102">ArgComplex function</span></span>

<span data-ttu-id="6fe61-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6fe61-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6fe61-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6fe61-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6fe61-105">Retourneert de fase van een complex type getal `Complex` .</span><span class="sxs-lookup"><span data-stu-id="6fe61-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="6fe61-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6fe61-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="6fe61-107">invoer: [complex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="6fe61-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="6fe61-108">Complex getal $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="6fe61-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="6fe61-109">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6fe61-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6fe61-110">Fase $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="6fe61-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>