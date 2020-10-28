---
uid: Microsoft.Quantum.Canon.Snd
title: De functie snd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c05053b45d24c3398526d1269b90bb40d1e0ef27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703815"
---
# <a name="snd-function"></a><span data-ttu-id="e0f8b-102">De functie snd</span><span class="sxs-lookup"><span data-stu-id="e0f8b-102">Snd function</span></span>

<span data-ttu-id="e0f8b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e0f8b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e0f8b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e0f8b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e0f8b-105">Retourneert het tweede element aan de hand van een paar.</span><span class="sxs-lookup"><span data-stu-id="e0f8b-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="e0f8b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e0f8b-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="e0f8b-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="e0f8b-107">pair : ('T,'U)</span></span>

<span data-ttu-id="e0f8b-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="e0f8b-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="e0f8b-109">Uitvoer: ' U</span><span class="sxs-lookup"><span data-stu-id="e0f8b-109">Output : 'U</span></span>

<span data-ttu-id="e0f8b-110">Het tweede element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="e0f8b-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e0f8b-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e0f8b-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e0f8b-112">T</span><span class="sxs-lookup"><span data-stu-id="e0f8b-112">'T</span></span>

<span data-ttu-id="e0f8b-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="e0f8b-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="e0f8b-114">' U</span><span class="sxs-lookup"><span data-stu-id="e0f8b-114">'U</span></span>

<span data-ttu-id="e0f8b-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="e0f8b-115">The type of the pair's second member.</span></span>