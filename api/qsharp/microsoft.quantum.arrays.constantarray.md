---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846231"
---
# <a name="constantarray-function"></a><span data-ttu-id="72177-102">De functie ConstantArray</span><span class="sxs-lookup"><span data-stu-id="72177-102">ConstantArray function</span></span>

<span data-ttu-id="72177-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="72177-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="72177-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72177-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72177-105">Maakt een matrix met de opgegeven lengte en alle elementen die gelijk zijn aan de opgegeven waarde.</span><span class="sxs-lookup"><span data-stu-id="72177-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="72177-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="72177-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="72177-107">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="72177-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="72177-108">Lengte van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="72177-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="72177-109">waarde: 'T</span><span class="sxs-lookup"><span data-stu-id="72177-109">value : 'T</span></span>

<span data-ttu-id="72177-110">De waarde van elk element van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="72177-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="72177-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="72177-111">Output : 'T[]</span></span>

<span data-ttu-id="72177-112">Een nieuwe matrix met lengte `length` , zodat elk element is `value` .</span><span class="sxs-lookup"><span data-stu-id="72177-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="72177-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="72177-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="72177-114">T</span><span class="sxs-lookup"><span data-stu-id="72177-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="72177-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="72177-115">Example</span></span>

<span data-ttu-id="72177-116">Met de volgende code wordt een matrix van drie Booleaanse waarden gemaakt die gelijk zijn aan `true` :</span><span class="sxs-lookup"><span data-stu-id="72177-116">The following code creates an array of 3 Boolean values, each equal to `true`:</span></span>

```qsharp
let array = ConstantArray(3, true);
```