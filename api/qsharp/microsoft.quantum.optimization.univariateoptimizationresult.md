---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194029"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="cdea2-102">Door de gebruiker gedefinieerd UnivariateOptimizationResult-type</span><span class="sxs-lookup"><span data-stu-id="cdea2-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="cdea2-103">Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="cdea2-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="cdea2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cdea2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cdea2-105">Hiermee wordt het resultaat van het optimaliseren van een univariate-functie aangeduid.</span><span class="sxs-lookup"><span data-stu-id="cdea2-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="cdea2-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="cdea2-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="cdea2-107">Coördinaat: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cdea2-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cdea2-108">Invoer waarbij een optimale bevinding is gevonden.</span><span class="sxs-lookup"><span data-stu-id="cdea2-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="cdea2-109">Waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cdea2-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cdea2-110">De waarde die is geretourneerd door de functie is optimaal.</span><span class="sxs-lookup"><span data-stu-id="cdea2-110">Value returned by the function at its optimum.</span></span>