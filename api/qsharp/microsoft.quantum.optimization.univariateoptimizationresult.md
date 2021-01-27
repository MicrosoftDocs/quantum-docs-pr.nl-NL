---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854572"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="873a4-102">Door de gebruiker gedefinieerd UnivariateOptimizationResult-type</span><span class="sxs-lookup"><span data-stu-id="873a4-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="873a4-103">Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="873a4-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="873a4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="873a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="873a4-105">Hiermee wordt het resultaat van het optimaliseren van een univariate-functie aangeduid.</span><span class="sxs-lookup"><span data-stu-id="873a4-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="873a4-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="873a4-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="873a4-107">Coördinaat: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="873a4-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="873a4-108">Invoer waarbij een optimale bevinding is gevonden.</span><span class="sxs-lookup"><span data-stu-id="873a4-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="873a4-109">Waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="873a4-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="873a4-110">De waarde die is geretourneerd door de functie is optimaal.</span><span class="sxs-lookup"><span data-stu-id="873a4-110">Value returned by the function at its optimum.</span></span>