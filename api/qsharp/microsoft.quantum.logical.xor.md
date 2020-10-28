---
uid: Microsoft.Quantum.Logical.Xor
title: Functie XOR
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: ae43545e19e81ed5da17c3d58c62ac0b7ee765f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708347"
---
# <a name="xor-function"></a><span data-ttu-id="86ec7-102">Functie XOR</span><span class="sxs-lookup"><span data-stu-id="86ec7-102">Xor function</span></span>

<span data-ttu-id="86ec7-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="86ec7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="86ec7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86ec7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86ec7-105">Retourneert de enige Booleaanse schei ding van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="86ec7-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="86ec7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="86ec7-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="86ec7-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="86ec7-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="86ec7-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="86ec7-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="86ec7-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="86ec7-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="86ec7-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="86ec7-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="86ec7-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="86ec7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="86ec7-112">`true` Als en alleen als dat zo `a` `b` is `true` .</span><span class="sxs-lookup"><span data-stu-id="86ec7-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>