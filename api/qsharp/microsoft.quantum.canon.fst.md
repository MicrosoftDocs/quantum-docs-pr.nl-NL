---
uid: Microsoft.Quantum.Canon.Fst
title: De functie FST
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704180"
---
# <a name="fst-function"></a><span data-ttu-id="8f995-102">De functie FST</span><span class="sxs-lookup"><span data-stu-id="8f995-102">Fst function</span></span>

<span data-ttu-id="8f995-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f995-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f995-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8f995-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8f995-105">Het eerste element wordt geretourneerd door een paar.</span><span class="sxs-lookup"><span data-stu-id="8f995-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="8f995-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8f995-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="8f995-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="8f995-107">pair : ('T,'U)</span></span>

<span data-ttu-id="8f995-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="8f995-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="8f995-109">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="8f995-109">Output : 'T</span></span>

<span data-ttu-id="8f995-110">Het eerste element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="8f995-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8f995-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8f995-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8f995-112">T</span><span class="sxs-lookup"><span data-stu-id="8f995-112">'T</span></span>

<span data-ttu-id="8f995-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="8f995-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="8f995-114">' U</span><span class="sxs-lookup"><span data-stu-id="8f995-114">'U</span></span>

<span data-ttu-id="8f995-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="8f995-115">The type of the pair's second member.</span></span>