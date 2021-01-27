---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: De functie WithZeroInsertedAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 7d5f8838b6ae555524fb0e82e14f93e6c77e43d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855201"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="857f5-102">De functie WithZeroInsertedAt</span><span class="sxs-lookup"><span data-stu-id="857f5-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="857f5-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="857f5-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="857f5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="857f5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="857f5-105">Een 0-bit invoegen in een geheel getal</span><span class="sxs-lookup"><span data-stu-id="857f5-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="857f5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="857f5-106">Description</span></span>

<span data-ttu-id="857f5-107">Voor deze bewerking wordt een geheel getal gebruikt, wordt een 0-bit ingevoegd `position` en wordt de bijgewerkte waarde als een geheel getal geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="857f5-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="857f5-108">Als u bijvoorbeeld een 0 op positie 2 in het getal 10 invoegt ($ 10 _ {10} = 1010_ {2} $), wordt het getal 18 als resultaat gegeven ($18 _ {10} = 10010_ {2} $).</span><span class="sxs-lookup"><span data-stu-id="857f5-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="857f5-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="857f5-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="857f5-110">positie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="857f5-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="857f5-111">De positie waarop 0 is ingevoegd</span><span class="sxs-lookup"><span data-stu-id="857f5-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="857f5-112">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="857f5-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="857f5-113">De waarde die is gewijzigd</span><span class="sxs-lookup"><span data-stu-id="857f5-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="857f5-114">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="857f5-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="857f5-115">Gewijzigde waarde</span><span class="sxs-lookup"><span data-stu-id="857f5-115">Modified value</span></span>