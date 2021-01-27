---
uid: Microsoft.Quantum.Arrays.Flattened
title: Platte functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848623"
---
# <a name="flattened-function"></a><span data-ttu-id="a105f-102">Platte functie</span><span class="sxs-lookup"><span data-stu-id="a105f-102">Flattened function</span></span>

<span data-ttu-id="a105f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a105f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a105f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a105f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a105f-105">Met een matrix van matrices wordt de samen voeging van alle matrices geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="a105f-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a105f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a105f-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="a105f-107">matrices: ' [] []</span><span class="sxs-lookup"><span data-stu-id="a105f-107">arrays : 'T[][]</span></span>

<span data-ttu-id="a105f-108">Matrix van matrices.</span><span class="sxs-lookup"><span data-stu-id="a105f-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="a105f-109">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="a105f-109">Output : 'T[]</span></span>

<span data-ttu-id="a105f-110">Samen voeging van alle matrices.</span><span class="sxs-lookup"><span data-stu-id="a105f-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a105f-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a105f-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a105f-112">T</span><span class="sxs-lookup"><span data-stu-id="a105f-112">'T</span></span>

<span data-ttu-id="a105f-113">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="a105f-113">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="a105f-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a105f-114">Example</span></span>

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```