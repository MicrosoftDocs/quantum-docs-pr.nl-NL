---
uid: Microsoft.Quantum.Intrinsic.Message
title: Bericht functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199009"
---
# <a name="message-function"></a><span data-ttu-id="81c4d-102">Bericht functie</span><span class="sxs-lookup"><span data-stu-id="81c4d-102">Message function</span></span>

<span data-ttu-id="81c4d-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="81c4d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="81c4d-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="81c4d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="81c4d-105">Een bericht wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="81c4d-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="81c4d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="81c4d-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="81c4d-107">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="81c4d-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="81c4d-108">Het bericht dat moet worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="81c4d-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="81c4d-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81c4d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="81c4d-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="81c4d-110">Remarks</span></span>

<span data-ttu-id="81c4d-111">Het specifieke gedrag van deze functie is van Simulator afhankelijk, maar in de meeste gevallen wordt het gegeven bericht naar de-console geschreven.</span><span class="sxs-lookup"><span data-stu-id="81c4d-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>