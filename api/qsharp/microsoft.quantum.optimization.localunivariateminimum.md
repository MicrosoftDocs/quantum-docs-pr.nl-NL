---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: De functie LocalUnivariateMinimum
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: 3b09af88bbed20a392768d005e5e9567b3bb7022
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701918"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="6ec1d-102">De functie LocalUnivariateMinimum</span><span class="sxs-lookup"><span data-stu-id="6ec1d-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="6ec1d-103">Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="6ec1d-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="6ec1d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6ec1d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6ec1d-105">Retourneert het lokale minimum voor een univariate-functie gedurende een beperkt interval, met behulp van een gouden interval zoekactie.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="6ec1d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6ec1d-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="6ec1d-107">FN: [dubbele](xref:microsoft.quantum.lang-ref.double) -> [dubbele precisie](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6ec1d-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6ec1d-108">De functie univariate die moet worden geminimaliseerd.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="6ec1d-109">grenzen: ([dubbel](xref:microsoft.quantum.lang-ref.double),[dubbel](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="6ec1d-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="6ec1d-110">Het interval waarin het lokale minimum moet worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="6ec1d-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6ec1d-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6ec1d-112">De nauw keurigheid van de functie-invoer die moet worden toegestaan.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="6ec1d-113">De zoek actie naar lokale Optima by wordt voortgezet totdat het interval kleiner is dan deze tolerantie.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="6ec1d-114">Uitvoer: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="6ec1d-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="6ec1d-115">Een lokale optimais van de opgegeven functie, die zich binnen de opgegeven grenzen bevindt.</span><span class="sxs-lookup"><span data-stu-id="6ec1d-115">A local optima of the given function, located within the given bounds.</span></span>