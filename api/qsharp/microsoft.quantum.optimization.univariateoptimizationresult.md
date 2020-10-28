---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708790"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="ef4b5-102">Door de gebruiker gedefinieerd UnivariateOptimizationResult-type</span><span class="sxs-lookup"><span data-stu-id="ef4b5-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="ef4b5-103">Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="ef4b5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ef4b5-105">Hiermee wordt het resultaat van het optimaliseren van een univariate-functie aangeduid.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="ef4b5-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="ef4b5-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="ef4b5-107">Coördinaat: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ef4b5-108">Invoer waarbij een optimale bevinding is gevonden.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="ef4b5-109">Waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ef4b5-110">De waarde die is geretourneerd door de functie is optimaal.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-110">Value returned by the function at its optimum.</span></span>