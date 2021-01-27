---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849073"
---
# <a name="not-function"></a><span data-ttu-id="449a4-102">Niet-functie</span><span class="sxs-lookup"><span data-stu-id="449a4-102">Not function</span></span>

<span data-ttu-id="449a4-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="449a4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="449a4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="449a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="449a4-105">Retourneert de Boole-ontkenning van een waarde.</span><span class="sxs-lookup"><span data-stu-id="449a4-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="449a4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="449a4-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="449a4-107">waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="449a4-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="449a4-108">De waarde die moet worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="449a4-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="449a4-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="449a4-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="449a4-110">`true` alleen als dat zo `value` is `false` .</span><span class="sxs-lookup"><span data-stu-id="449a4-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="449a4-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="449a4-111">Remarks</span></span>

<span data-ttu-id="449a4-112">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="449a4-112">The following are equivalent:</span></span>

```qsharp
let x = not value;
let x = Not(value);
```