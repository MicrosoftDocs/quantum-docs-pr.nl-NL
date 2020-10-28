---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701421"
---
# <a name="not-function"></a><span data-ttu-id="285ad-102">Niet-functie</span><span class="sxs-lookup"><span data-stu-id="285ad-102">Not function</span></span>

<span data-ttu-id="285ad-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="285ad-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="285ad-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="285ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="285ad-105">Retourneert de Boole-ontkenning van een waarde.</span><span class="sxs-lookup"><span data-stu-id="285ad-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="285ad-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="285ad-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="285ad-107">waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="285ad-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="285ad-108">De waarde die moet worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="285ad-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="285ad-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="285ad-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="285ad-110">`true` alleen als dat zo `value` is `false` .</span><span class="sxs-lookup"><span data-stu-id="285ad-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="285ad-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="285ad-111">Remarks</span></span>

<span data-ttu-id="285ad-112">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="285ad-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```