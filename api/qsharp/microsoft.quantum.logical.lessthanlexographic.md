---
uid: Microsoft.Quantum.Logical.LessThanLexographic
title: De functie LessThanLexographic
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanLexographic
qsharp.summary: Used to implement `LexographicComparison`.
ms.openlocfilehash: 716f58b747e9f58c338670271bb2e7aed96fe98c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815647"
---
# <a name="lessthanlexographic-function"></a><span data-ttu-id="357f0-102">De functie LessThanLexographic</span><span class="sxs-lookup"><span data-stu-id="357f0-102">LessThanLexographic function</span></span>

<span data-ttu-id="357f0-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="357f0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="357f0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="357f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="357f0-105">Wordt geïmplementeerd `LexographicComparison` .</span><span class="sxs-lookup"><span data-stu-id="357f0-105">Used to implement `LexographicComparison`.</span></span>

```qsharp
function LessThanLexographic<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="357f0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="357f0-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="357f0-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="357f0-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="357f0-108">links: ' []</span><span class="sxs-lookup"><span data-stu-id="357f0-108">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="357f0-109">rechts: ' []</span><span class="sxs-lookup"><span data-stu-id="357f0-109">right : 'T[]</span></span>





## <a name="output--bool"></a><span data-ttu-id="357f0-110">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="357f0-110">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="357f0-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="357f0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="357f0-112">T</span><span class="sxs-lookup"><span data-stu-id="357f0-112">'T</span></span>

