---
uid: Microsoft.Quantum.Logical.Xor
title: Functie XOR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: afb94bd1fd0b791a9a7d84bc28b0cc2baf9a0938
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197089"
---
# <a name="xor-function"></a><span data-ttu-id="5539e-102">Functie XOR</span><span class="sxs-lookup"><span data-stu-id="5539e-102">Xor function</span></span>

<span data-ttu-id="5539e-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5539e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5539e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5539e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5539e-105">Retourneert de enige Booleaanse schei ding van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="5539e-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="5539e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5539e-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="5539e-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5539e-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5539e-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="5539e-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="5539e-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5539e-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5539e-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="5539e-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5539e-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5539e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5539e-112">`true` Als en alleen als dat zo `a` `b` is `true` .</span><span class="sxs-lookup"><span data-stu-id="5539e-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>