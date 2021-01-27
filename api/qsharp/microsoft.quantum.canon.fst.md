---
uid: Microsoft.Quantum.Canon.Fst
title: De functie FST
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840523"
---
# <a name="fst-function"></a><span data-ttu-id="64408-102">De functie FST</span><span class="sxs-lookup"><span data-stu-id="64408-102">Fst function</span></span>

<span data-ttu-id="64408-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="64408-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="64408-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64408-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64408-105">Het eerste element wordt geretourneerd door een paar.</span><span class="sxs-lookup"><span data-stu-id="64408-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="64408-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="64408-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="64408-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="64408-107">pair : ('T,'U)</span></span>

<span data-ttu-id="64408-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="64408-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="64408-109">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="64408-109">Output : 'T</span></span>

<span data-ttu-id="64408-110">Het eerste element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="64408-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="64408-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="64408-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64408-112">T</span><span class="sxs-lookup"><span data-stu-id="64408-112">'T</span></span>

<span data-ttu-id="64408-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="64408-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="64408-114">' U</span><span class="sxs-lookup"><span data-stu-id="64408-114">'U</span></span>

<span data-ttu-id="64408-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="64408-115">The type of the pair's second member.</span></span>