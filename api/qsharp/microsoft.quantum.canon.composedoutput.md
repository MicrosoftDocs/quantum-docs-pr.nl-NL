---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: De functie ComposedOutput
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 7e361a62679ab93e9a0ebc04fa52be193805c78d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207459"
---
# <a name="composedoutput-function"></a><span data-ttu-id="89f22-102">De functie ComposedOutput</span><span class="sxs-lookup"><span data-stu-id="89f22-102">ComposedOutput function</span></span>

<span data-ttu-id="89f22-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="89f22-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="89f22-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="89f22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="89f22-105">Retourneert de uitvoer van de samen stelling van `inner` en `outer` voor een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="89f22-105">Returns the output of the composition of `inner` and `outer` for a given input.</span></span>

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a><span data-ttu-id="89f22-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="89f22-106">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="89f22-107">Outer: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="89f22-107">outer : 'U -> 'V</span></span>




### <a name="inner--t---u"></a><span data-ttu-id="89f22-108">binnenste: 'T-> ' U</span><span class="sxs-lookup"><span data-stu-id="89f22-108">inner : 'T -> 'U</span></span>




### <a name="target--t"></a><span data-ttu-id="89f22-109">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="89f22-109">target : 'T</span></span>





## <a name="output--v"></a><span data-ttu-id="89f22-110">Uitvoer: ' V</span><span class="sxs-lookup"><span data-stu-id="89f22-110">Output : 'V</span></span>



## <a name="type-parameters"></a><span data-ttu-id="89f22-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="89f22-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="89f22-112">T</span><span class="sxs-lookup"><span data-stu-id="89f22-112">'T</span></span>


### <a name="u"></a><span data-ttu-id="89f22-113">' U</span><span class="sxs-lookup"><span data-stu-id="89f22-113">'U</span></span>


### <a name="v"></a><span data-ttu-id="89f22-114">' V</span><span class="sxs-lookup"><span data-stu-id="89f22-114">'V</span></span>

