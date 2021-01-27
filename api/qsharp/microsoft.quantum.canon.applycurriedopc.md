---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: Bewerking ApplyCurriedOpC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 65e861914b57cf8a32f2321f881248830b72c54e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841913"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="a2be1-102">Bewerking ApplyCurriedOpC</span><span class="sxs-lookup"><span data-stu-id="a2be1-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="a2be1-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a2be1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a2be1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2be1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="a2be1-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="a2be1-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="a2be1-106">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="a2be1-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="a2be1-107">eerst: 'T</span><span class="sxs-lookup"><span data-stu-id="a2be1-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="a2be1-108">seconde: ' U</span><span class="sxs-lookup"><span data-stu-id="a2be1-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="a2be1-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2be1-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a2be1-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a2be1-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a2be1-111">T</span><span class="sxs-lookup"><span data-stu-id="a2be1-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="a2be1-112">' U</span><span class="sxs-lookup"><span data-stu-id="a2be1-112">'U</span></span>

