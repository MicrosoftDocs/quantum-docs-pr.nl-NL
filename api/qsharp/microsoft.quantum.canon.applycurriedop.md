---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: Bewerking ApplyCurriedOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: ab652159fa64a95401d07998ed4aaae5c4dbb92e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219019"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="5d5e1-102">Bewerking ApplyCurriedOp</span><span class="sxs-lookup"><span data-stu-id="5d5e1-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="5d5e1-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5d5e1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5d5e1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d5e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="5d5e1-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="5d5e1-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="5d5e1-106">curriedOp: 'T-> ' U =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d5e1-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="5d5e1-107">eerst: 'T</span><span class="sxs-lookup"><span data-stu-id="5d5e1-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="5d5e1-108">seconde: ' U</span><span class="sxs-lookup"><span data-stu-id="5d5e1-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="5d5e1-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d5e1-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5d5e1-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5d5e1-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5d5e1-111">T</span><span class="sxs-lookup"><span data-stu-id="5d5e1-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="5d5e1-112">' U</span><span class="sxs-lookup"><span data-stu-id="5d5e1-112">'U</span></span>

