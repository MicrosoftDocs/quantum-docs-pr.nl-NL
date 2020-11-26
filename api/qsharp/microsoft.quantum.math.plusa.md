---
uid: Microsoft.Quantum.Math.PlusA
title: Functie plus
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: fe19c5d2e075624516376a5d5fa49014acb295ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194828"
---
# <a name="plusa-function"></a><span data-ttu-id="4546a-102">Functie plus</span><span class="sxs-lookup"><span data-stu-id="4546a-102">PlusA function</span></span>

<span data-ttu-id="4546a-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4546a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4546a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4546a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4546a-105">Retourneert de som (samen voeging) van twee invoer waarden.</span><span class="sxs-lookup"><span data-stu-id="4546a-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="4546a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4546a-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="4546a-107">a:-element []</span><span class="sxs-lookup"><span data-stu-id="4546a-107">a : 'Element[]</span></span>

<span data-ttu-id="4546a-108">De eerste invoer $a $ die moet worden opgeteld.</span><span class="sxs-lookup"><span data-stu-id="4546a-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="4546a-109">b: element []</span><span class="sxs-lookup"><span data-stu-id="4546a-109">b : 'Element[]</span></span>

<span data-ttu-id="4546a-110">De tweede invoer $b $ moet worden opgeteld.</span><span class="sxs-lookup"><span data-stu-id="4546a-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="4546a-111">Output: ' element []</span><span class="sxs-lookup"><span data-stu-id="4546a-111">Output : 'Element[]</span></span>

<span data-ttu-id="4546a-112">De som $a + b $.</span><span class="sxs-lookup"><span data-stu-id="4546a-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4546a-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="4546a-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="4546a-114">Element</span><span class="sxs-lookup"><span data-stu-id="4546a-114">'Element</span></span>

<span data-ttu-id="4546a-115">Het type van elk element in elk van de twee invoer matrices.</span><span class="sxs-lookup"><span data-stu-id="4546a-115">The type of each element in each of the two input arrays.</span></span>