---
uid: Microsoft.Quantum.Arrays.Merged
title: Samengevoegde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845613"
---
# <a name="merged-function"></a><span data-ttu-id="e37ae-102">Samengevoegde functie</span><span class="sxs-lookup"><span data-stu-id="e37ae-102">Merged function</span></span>

<span data-ttu-id="e37ae-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e37ae-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e37ae-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e37ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e37ae-105">Als er twee gesorteerde matrices worden opgegeven, wordt er één matrix met de elementen van beide in gesorteerde volg orde geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e37ae-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="e37ae-106">Intern gebruikt door samen voegen sorteren.</span><span class="sxs-lookup"><span data-stu-id="e37ae-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e37ae-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="e37ae-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="e37ae-108">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e37ae-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="e37ae-109">links: ' []</span><span class="sxs-lookup"><span data-stu-id="e37ae-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="e37ae-110">rechts: ' []</span><span class="sxs-lookup"><span data-stu-id="e37ae-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="e37ae-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="e37ae-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e37ae-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e37ae-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e37ae-113">T</span><span class="sxs-lookup"><span data-stu-id="e37ae-113">'T</span></span>

