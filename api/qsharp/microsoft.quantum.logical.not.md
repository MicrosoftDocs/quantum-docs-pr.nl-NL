---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197446"
---
# <a name="not-function"></a><span data-ttu-id="20a5c-102">Niet-functie</span><span class="sxs-lookup"><span data-stu-id="20a5c-102">Not function</span></span>

<span data-ttu-id="20a5c-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="20a5c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="20a5c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20a5c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20a5c-105">Retourneert de Boole-ontkenning van een waarde.</span><span class="sxs-lookup"><span data-stu-id="20a5c-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="20a5c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="20a5c-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="20a5c-107">waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="20a5c-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="20a5c-108">De waarde die moet worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="20a5c-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="20a5c-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="20a5c-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="20a5c-110">`true` alleen als dat zo `value` is `false` .</span><span class="sxs-lookup"><span data-stu-id="20a5c-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a5c-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="20a5c-111">Remarks</span></span>

<span data-ttu-id="20a5c-112">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="20a5c-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```