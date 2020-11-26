---
uid: Microsoft.Quantum.Canon.Snd
title: De functie snd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205317"
---
# <a name="snd-function"></a><span data-ttu-id="9b096-102">De functie snd</span><span class="sxs-lookup"><span data-stu-id="9b096-102">Snd function</span></span>

<span data-ttu-id="9b096-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9b096-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9b096-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b096-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b096-105">Retourneert het tweede element aan de hand van een paar.</span><span class="sxs-lookup"><span data-stu-id="9b096-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="9b096-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9b096-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="9b096-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="9b096-107">pair : ('T,'U)</span></span>

<span data-ttu-id="9b096-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="9b096-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="9b096-109">Uitvoer: ' U</span><span class="sxs-lookup"><span data-stu-id="9b096-109">Output : 'U</span></span>

<span data-ttu-id="9b096-110">Het tweede element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="9b096-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9b096-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9b096-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9b096-112">T</span><span class="sxs-lookup"><span data-stu-id="9b096-112">'T</span></span>

<span data-ttu-id="9b096-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="9b096-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="9b096-114">' U</span><span class="sxs-lookup"><span data-stu-id="9b096-114">'U</span></span>

<span data-ttu-id="9b096-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="9b096-115">The type of the pair's second member.</span></span>