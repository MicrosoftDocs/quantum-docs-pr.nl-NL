---
uid: Microsoft.Quantum.Canon.Compose
title: Functie voor opstellen
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840908"
---
# <a name="compose-function"></a><span data-ttu-id="d9ccc-102">Functie voor opstellen</span><span class="sxs-lookup"><span data-stu-id="d9ccc-102">Compose function</span></span>

<span data-ttu-id="d9ccc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d9ccc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d9ccc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9ccc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d9ccc-105">Retourneert de samen stelling van twee functies.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="d9ccc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d9ccc-106">Description</span></span>

<span data-ttu-id="d9ccc-107">Als er twee functies $f $ en $g $ worden opgegeven, wordt een nieuwe functie geretourneerd die $f \circ g $ vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="d9ccc-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d9ccc-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="d9ccc-109">Outer: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="d9ccc-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="d9ccc-110">De tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="d9ccc-111">binnenste: 'T-> ' U</span><span class="sxs-lookup"><span data-stu-id="d9ccc-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="d9ccc-112">De eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="d9ccc-113">Uitvoer: niet-> ' V</span><span class="sxs-lookup"><span data-stu-id="d9ccc-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="d9ccc-114">Een nieuwe functie $h $, zoals voor alle invoer waarden $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d9ccc-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d9ccc-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d9ccc-116">T</span><span class="sxs-lookup"><span data-stu-id="d9ccc-116">'T</span></span>

<span data-ttu-id="d9ccc-117">Het invoer type van de eerste functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="d9ccc-118">' U</span><span class="sxs-lookup"><span data-stu-id="d9ccc-118">'U</span></span>

<span data-ttu-id="d9ccc-119">Het uitvoer type van de eerste functie die moet worden toegepast en het invoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="d9ccc-120">' V</span><span class="sxs-lookup"><span data-stu-id="d9ccc-120">'V</span></span>

<span data-ttu-id="d9ccc-121">Het uitvoer type van de tweede functie die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9ccc-121">The output type of the second function to be applied.</span></span>