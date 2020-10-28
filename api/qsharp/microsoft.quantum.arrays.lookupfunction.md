---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: De functie LookupFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705909"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="d3a22-102">De functie LookupFunction</span><span class="sxs-lookup"><span data-stu-id="d3a22-102">LookupFunction function</span></span>

<span data-ttu-id="d3a22-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d3a22-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d3a22-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3a22-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3a22-105">Retourneert een functie die elementen van die matrix retourneert, uitgedrukt in een matrix.</span><span class="sxs-lookup"><span data-stu-id="d3a22-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="d3a22-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d3a22-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="d3a22-107">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="d3a22-107">array : 'T[]</span></span>

<span data-ttu-id="d3a22-108">De matrix die moet worden weer gegeven als een opzoek functie.</span><span class="sxs-lookup"><span data-stu-id="d3a22-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="d3a22-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int) -> niet</span><span class="sxs-lookup"><span data-stu-id="d3a22-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="d3a22-110">Een functie `f` `f(idx) == f[idx]` .</span><span class="sxs-lookup"><span data-stu-id="d3a22-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d3a22-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d3a22-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d3a22-112">T</span><span class="sxs-lookup"><span data-stu-id="d3a22-112">'T</span></span>

<span data-ttu-id="d3a22-113">Het type van de elementen van de matrix die wordt weer gegeven als een opzoek functie.</span><span class="sxs-lookup"><span data-stu-id="d3a22-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a22-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d3a22-114">Remarks</span></span>

<span data-ttu-id="d3a22-115">Deze functie is vooral nuttig voor het samen werken met functies en bewerkingen die `Int -> 'T` functies als argumenten hebben.</span><span class="sxs-lookup"><span data-stu-id="d3a22-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="d3a22-116">Dit is bijvoorbeeld gebruikelijk in de representatieve generator, waarbij functies worden gebruikt om te voor komen dat een volledige matrix in het geheugen hoeft te worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="d3a22-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>