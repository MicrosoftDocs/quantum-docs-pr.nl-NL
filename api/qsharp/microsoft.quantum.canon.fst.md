---
uid: Microsoft.Quantum.Canon.Fst
title: De functie FST
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206932"
---
# <a name="fst-function"></a><span data-ttu-id="d6249-102">De functie FST</span><span class="sxs-lookup"><span data-stu-id="d6249-102">Fst function</span></span>

<span data-ttu-id="d6249-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d6249-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d6249-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6249-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6249-105">Het eerste element wordt geretourneerd door een paar.</span><span class="sxs-lookup"><span data-stu-id="d6249-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="d6249-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d6249-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="d6249-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="d6249-107">pair : ('T,'U)</span></span>

<span data-ttu-id="d6249-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="d6249-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="d6249-109">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="d6249-109">Output : 'T</span></span>

<span data-ttu-id="d6249-110">Het eerste element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="d6249-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d6249-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d6249-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d6249-112">T</span><span class="sxs-lookup"><span data-stu-id="d6249-112">'T</span></span>

<span data-ttu-id="d6249-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="d6249-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="d6249-114">' U</span><span class="sxs-lookup"><span data-stu-id="d6249-114">'U</span></span>

<span data-ttu-id="d6249-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="d6249-115">The type of the pair's second member.</span></span>