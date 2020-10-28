---
uid: Microsoft.Quantum.Canon.Compose
title: Functie voor opstellen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704356"
---
# <a name="compose-function"></a><span data-ttu-id="0140d-102">Functie voor opstellen</span><span class="sxs-lookup"><span data-stu-id="0140d-102">Compose function</span></span>

<span data-ttu-id="0140d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0140d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0140d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0140d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0140d-105">Retourneert de samen stelling van twee functies.</span><span class="sxs-lookup"><span data-stu-id="0140d-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="0140d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0140d-106">Description</span></span>

<span data-ttu-id="0140d-107">Als er twee functies $f $ en $g $ worden opgegeven, wordt een nieuwe functie geretourneerd die $f \circ g $ vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="0140d-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="0140d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="0140d-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="0140d-109">Outer: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="0140d-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="0140d-110">De tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="0140d-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="0140d-111">binnenste: 'T-> ' U</span><span class="sxs-lookup"><span data-stu-id="0140d-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="0140d-112">De eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="0140d-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="0140d-113">Uitvoer: niet-> ' V</span><span class="sxs-lookup"><span data-stu-id="0140d-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="0140d-114">Een nieuwe functie $h $, zoals voor alle invoer waarden $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="0140d-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0140d-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="0140d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0140d-116">T</span><span class="sxs-lookup"><span data-stu-id="0140d-116">'T</span></span>

<span data-ttu-id="0140d-117">Het invoer type van de eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="0140d-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="0140d-118">' U</span><span class="sxs-lookup"><span data-stu-id="0140d-118">'U</span></span>

<span data-ttu-id="0140d-119">Het uitvoer type van de eerste functie die moet worden toegepast en het invoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="0140d-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="0140d-120">' V</span><span class="sxs-lookup"><span data-stu-id="0140d-120">'V</span></span>

<span data-ttu-id="0140d-121">Het uitvoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="0140d-121">The output type of the second function to be applied.</span></span>