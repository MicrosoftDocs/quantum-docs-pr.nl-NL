---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpCA
title: Bewerking ApplyCurriedOpCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpCA
qsharp.summary: ''
ms.openlocfilehash: df534a3156ac3f5411161c6faf4d39759e49fbed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218900"
---
# <a name="applycurriedopca-operation"></a><span data-ttu-id="dc9fc-102">Bewerking ApplyCurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="dc9fc-102">ApplyCurriedOpCA operation</span></span>

<span data-ttu-id="dc9fc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dc9fc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dc9fc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dc9fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj)), first : 'T, second : 'U) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dc9fc-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="dc9fc-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="dc9fc-106">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="dc9fc-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="dc9fc-107">eerst: 'T</span><span class="sxs-lookup"><span data-stu-id="dc9fc-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="dc9fc-108">seconde: ' U</span><span class="sxs-lookup"><span data-stu-id="dc9fc-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="dc9fc-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dc9fc-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dc9fc-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dc9fc-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dc9fc-111">T</span><span class="sxs-lookup"><span data-stu-id="dc9fc-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="dc9fc-112">' U</span><span class="sxs-lookup"><span data-stu-id="dc9fc-112">'U</span></span>

