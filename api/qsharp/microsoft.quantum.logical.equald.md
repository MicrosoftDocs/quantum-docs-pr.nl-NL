---
uid: Microsoft.Quantum.Logical.EqualD
title: Functie is gelijk aan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 024ddee785a6a907b4a39d0eccc5990b4c5d5d83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702080"
---
# <a name="equald-function"></a><span data-ttu-id="cd521-102">Functie is gelijk aan</span><span class="sxs-lookup"><span data-stu-id="cd521-102">EqualD function</span></span>

<span data-ttu-id="cd521-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cd521-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cd521-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cd521-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cd521-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="cd521-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="cd521-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd521-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="cd521-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cd521-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cd521-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cd521-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="cd521-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cd521-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cd521-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cd521-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cd521-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cd521-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cd521-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="cd521-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd521-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cd521-113">Remarks</span></span>

<span data-ttu-id="cd521-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="cd521-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```