---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: De functie WithZeroInsertedAt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 6e13251741dadb19740b208cdfc13a14964a48dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709145"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="35264-102">De functie WithZeroInsertedAt</span><span class="sxs-lookup"><span data-stu-id="35264-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="35264-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="35264-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="35264-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="35264-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="35264-105">Een 0-bit invoegen in een geheel getal</span><span class="sxs-lookup"><span data-stu-id="35264-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="35264-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="35264-106">Description</span></span>

<span data-ttu-id="35264-107">Voor deze bewerking wordt een geheel getal gebruikt, wordt een 0-bit ingevoegd `position` en wordt de bijgewerkte waarde als een geheel getal geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="35264-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="35264-108">Als u bijvoorbeeld een 0 op positie 2 in het getal 10 invoegt ($ 10 _ {10} = 1010_ {2} $), wordt het getal 18 als resultaat gegeven ($18 _ {10} = 10010_ {2} $).</span><span class="sxs-lookup"><span data-stu-id="35264-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="35264-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="35264-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="35264-110">positie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="35264-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="35264-111">De positie waarop 0 is ingevoegd</span><span class="sxs-lookup"><span data-stu-id="35264-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="35264-112">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="35264-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="35264-113">De waarde die is gewijzigd</span><span class="sxs-lookup"><span data-stu-id="35264-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="35264-114">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="35264-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="35264-115">Gewijzigde waarde</span><span class="sxs-lookup"><span data-stu-id="35264-115">Modified value</span></span>