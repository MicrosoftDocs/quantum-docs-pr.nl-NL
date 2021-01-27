---
uid: Microsoft.Quantum.Canon.Snd
title: De functie snd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: 11786fa195de12a7f2e4f2edb00ac0bc1071dd5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852159"
---
# <a name="snd-function"></a><span data-ttu-id="84878-102">De functie snd</span><span class="sxs-lookup"><span data-stu-id="84878-102">Snd function</span></span>

<span data-ttu-id="84878-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84878-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84878-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84878-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84878-105">Retourneert het tweede element aan de hand van een paar.</span><span class="sxs-lookup"><span data-stu-id="84878-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="84878-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="84878-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="84878-107">paar: ('T, ' U ')</span><span class="sxs-lookup"><span data-stu-id="84878-107">pair : ('T,'U)</span></span>

<span data-ttu-id="84878-108">Een tuple met twee elementen.</span><span class="sxs-lookup"><span data-stu-id="84878-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="84878-109">Uitvoer: ' U</span><span class="sxs-lookup"><span data-stu-id="84878-109">Output : 'U</span></span>

<span data-ttu-id="84878-110">Het tweede element van `pair` .</span><span class="sxs-lookup"><span data-stu-id="84878-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84878-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="84878-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84878-112">T</span><span class="sxs-lookup"><span data-stu-id="84878-112">'T</span></span>

<span data-ttu-id="84878-113">Het type van het eerste lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="84878-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="84878-114">' U</span><span class="sxs-lookup"><span data-stu-id="84878-114">'U</span></span>

<span data-ttu-id="84878-115">Het type van het tweede lid van het paar.</span><span class="sxs-lookup"><span data-stu-id="84878-115">The type of the pair's second member.</span></span>