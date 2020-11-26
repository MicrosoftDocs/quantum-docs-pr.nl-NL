---
uid: Microsoft.Quantum.Logical.LessThanLexographic
title: De functie LessThanLexographic
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanLexographic
qsharp.summary: Used to implement `LexographicComparison`.
ms.openlocfilehash: 3b3ac3f9f8b70307099de60899c969abb2acad7c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197667"
---
# <a name="lessthanlexographic-function"></a><span data-ttu-id="a2bb3-102">De functie LessThanLexographic</span><span class="sxs-lookup"><span data-stu-id="a2bb3-102">LessThanLexographic function</span></span>

<span data-ttu-id="a2bb3-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a2bb3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a2bb3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2bb3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a2bb3-105">Wordt geïmplementeerd `LexographicComparison` .</span><span class="sxs-lookup"><span data-stu-id="a2bb3-105">Used to implement `LexographicComparison`.</span></span>

```qsharp
function LessThanLexographic<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="a2bb3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a2bb3-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="a2bb3-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a2bb3-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="a2bb3-108">links: ' []</span><span class="sxs-lookup"><span data-stu-id="a2bb3-108">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="a2bb3-109">rechts: ' []</span><span class="sxs-lookup"><span data-stu-id="a2bb3-109">right : 'T[]</span></span>





## <a name="output--bool"></a><span data-ttu-id="a2bb3-110">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a2bb3-110">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a2bb3-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a2bb3-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a2bb3-112">T</span><span class="sxs-lookup"><span data-stu-id="a2bb3-112">'T</span></span>

