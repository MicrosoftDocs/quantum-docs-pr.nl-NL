---
uid: Microsoft.Quantum.Arrays.Merged
title: Samengevoegde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: b3383f8a04e6fa23562aa81e5b911d06752f4fb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220634"
---
# <a name="merged-function"></a><span data-ttu-id="8bec8-102">Samengevoegde functie</span><span class="sxs-lookup"><span data-stu-id="8bec8-102">Merged function</span></span>

<span data-ttu-id="8bec8-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8bec8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8bec8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8bec8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8bec8-105">Als er twee gesorteerde matrices worden opgegeven, wordt er één matrix met de elementen van beide in gesorteerde volg orde geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8bec8-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="8bec8-106">Intern gebruikt door samen voegen sorteren.</span><span class="sxs-lookup"><span data-stu-id="8bec8-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8bec8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="8bec8-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="8bec8-108">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8bec8-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="8bec8-109">links: ' []</span><span class="sxs-lookup"><span data-stu-id="8bec8-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="8bec8-110">rechts: ' []</span><span class="sxs-lookup"><span data-stu-id="8bec8-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="8bec8-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="8bec8-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8bec8-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8bec8-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8bec8-113">T</span><span class="sxs-lookup"><span data-stu-id="8bec8-113">'T</span></span>

