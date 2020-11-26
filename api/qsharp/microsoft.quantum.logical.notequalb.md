---
uid: Microsoft.Quantum.Logical.NotEqualB
title: De functie NotEqualB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 7943411b662683df058213a9e4b8eb7c9329ff07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197378"
---
# <a name="notequalb-function"></a><span data-ttu-id="f857f-102">De functie NotEqualB</span><span class="sxs-lookup"><span data-stu-id="f857f-102">NotEqualB function</span></span>

<span data-ttu-id="f857f-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f857f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f857f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f857f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f857f-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="f857f-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="f857f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f857f-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="f857f-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f857f-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f857f-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f857f-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="f857f-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f857f-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f857f-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f857f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f857f-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f857f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f857f-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="f857f-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f857f-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f857f-113">Remarks</span></span>

<span data-ttu-id="f857f-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="f857f-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```