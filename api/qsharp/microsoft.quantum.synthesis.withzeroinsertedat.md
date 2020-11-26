---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: De functie WithZeroInsertedAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228862"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="6ebb4-102">De functie WithZeroInsertedAt</span><span class="sxs-lookup"><span data-stu-id="6ebb4-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="6ebb4-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6ebb4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6ebb4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6ebb4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6ebb4-105">Een 0-bit invoegen in een geheel getal</span><span class="sxs-lookup"><span data-stu-id="6ebb4-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="6ebb4-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6ebb4-106">Description</span></span>

<span data-ttu-id="6ebb4-107">Voor deze bewerking wordt een geheel getal gebruikt, wordt een 0-bit ingevoegd `position` en wordt de bijgewerkte waarde als een geheel getal geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="6ebb4-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="6ebb4-108">Als u bijvoorbeeld een 0 op positie 2 in het getal 10 invoegt ($ 10 _ {10} = 1010_ {2} $), wordt het getal 18 als resultaat gegeven ($18 _ {10} = 10010_ {2} $).</span><span class="sxs-lookup"><span data-stu-id="6ebb4-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="6ebb4-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="6ebb4-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="6ebb4-110">positie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6ebb4-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6ebb4-111">De positie waarop 0 is ingevoegd</span><span class="sxs-lookup"><span data-stu-id="6ebb4-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="6ebb4-112">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6ebb4-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6ebb4-113">De waarde die is gewijzigd</span><span class="sxs-lookup"><span data-stu-id="6ebb4-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="6ebb4-114">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6ebb4-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6ebb4-115">Gewijzigde waarde</span><span class="sxs-lookup"><span data-stu-id="6ebb4-115">Modified value</span></span>