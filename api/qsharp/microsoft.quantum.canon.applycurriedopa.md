---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpA
title: Bewerking ApplyCurriedOpA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpA
qsharp.summary: ''
ms.openlocfilehash: 100d8a42d6475d3cdda349a2e685a6fbfff23cdc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845079"
---
# <a name="applycurriedopa-operation"></a><span data-ttu-id="ebd85-102">Bewerking ApplyCurriedOpA</span><span class="sxs-lookup"><span data-stu-id="ebd85-102">ApplyCurriedOpA operation</span></span>

<span data-ttu-id="ebd85-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ebd85-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ebd85-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ebd85-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj)), first : 'T, second : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="ebd85-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="ebd85-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="ebd85-106">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="ebd85-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="first--t"></a><span data-ttu-id="ebd85-107">eerst: 'T</span><span class="sxs-lookup"><span data-stu-id="ebd85-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="ebd85-108">seconde: ' U</span><span class="sxs-lookup"><span data-stu-id="ebd85-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="ebd85-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ebd85-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ebd85-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ebd85-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ebd85-111">T</span><span class="sxs-lookup"><span data-stu-id="ebd85-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="ebd85-112">' U</span><span class="sxs-lookup"><span data-stu-id="ebd85-112">'U</span></span>

