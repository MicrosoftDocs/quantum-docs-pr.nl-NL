---
uid: Microsoft.Quantum.Canon.Compose
title: Functie voor opstellen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216758"
---
# <a name="compose-function"></a><span data-ttu-id="c6dc0-102">Functie voor opstellen</span><span class="sxs-lookup"><span data-stu-id="c6dc0-102">Compose function</span></span>

<span data-ttu-id="c6dc0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c6dc0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c6dc0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c6dc0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c6dc0-105">Retourneert de samen stelling van twee functies.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="c6dc0-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c6dc0-106">Description</span></span>

<span data-ttu-id="c6dc0-107">Als er twee functies $f $ en $g $ worden opgegeven, wordt een nieuwe functie geretourneerd die $f \circ g $ vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="c6dc0-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c6dc0-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="c6dc0-109">Outer: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="c6dc0-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="c6dc0-110">De tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="c6dc0-111">binnenste: 'T-> ' U</span><span class="sxs-lookup"><span data-stu-id="c6dc0-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="c6dc0-112">De eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="c6dc0-113">Uitvoer: niet-> ' V</span><span class="sxs-lookup"><span data-stu-id="c6dc0-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="c6dc0-114">Een nieuwe functie $h $, zoals voor alle invoer waarden $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c6dc0-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c6dc0-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c6dc0-116">T</span><span class="sxs-lookup"><span data-stu-id="c6dc0-116">'T</span></span>

<span data-ttu-id="c6dc0-117">Het invoer type van de eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="c6dc0-118">' U</span><span class="sxs-lookup"><span data-stu-id="c6dc0-118">'U</span></span>

<span data-ttu-id="c6dc0-119">Het uitvoer type van de eerste functie die moet worden toegepast en het invoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="c6dc0-120">' V</span><span class="sxs-lookup"><span data-stu-id="c6dc0-120">'V</span></span>

<span data-ttu-id="c6dc0-121">Het uitvoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c6dc0-121">The output type of the second function to be applied.</span></span>