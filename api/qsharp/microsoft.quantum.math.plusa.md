---
uid: Microsoft.Quantum.Math.PlusA
title: Functie plus
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701312"
---
# <a name="plusa-function"></a><span data-ttu-id="667c4-102">Functie plus</span><span class="sxs-lookup"><span data-stu-id="667c4-102">PlusA function</span></span>

<span data-ttu-id="667c4-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="667c4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="667c4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="667c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="667c4-105">Retourneert de som (samen voeging) van twee invoer waarden.</span><span class="sxs-lookup"><span data-stu-id="667c4-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="667c4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="667c4-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="667c4-107">a:-element []</span><span class="sxs-lookup"><span data-stu-id="667c4-107">a : 'Element[]</span></span>

<span data-ttu-id="667c4-108">De eerste invoer $a $ die moet worden opgeteld.</span><span class="sxs-lookup"><span data-stu-id="667c4-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="667c4-109">b: element []</span><span class="sxs-lookup"><span data-stu-id="667c4-109">b : 'Element[]</span></span>

<span data-ttu-id="667c4-110">De tweede invoer $b $ moet worden opgeteld.</span><span class="sxs-lookup"><span data-stu-id="667c4-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="667c4-111">Output: ' element []</span><span class="sxs-lookup"><span data-stu-id="667c4-111">Output : 'Element[]</span></span>

<span data-ttu-id="667c4-112">De som $a + b $.</span><span class="sxs-lookup"><span data-stu-id="667c4-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="667c4-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="667c4-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="667c4-114">Element</span><span class="sxs-lookup"><span data-stu-id="667c4-114">'Element</span></span>

<span data-ttu-id="667c4-115">Het type van elk element in elk van de twee invoer matrices.</span><span class="sxs-lookup"><span data-stu-id="667c4-115">The type of each element in each of the two input arrays.</span></span>