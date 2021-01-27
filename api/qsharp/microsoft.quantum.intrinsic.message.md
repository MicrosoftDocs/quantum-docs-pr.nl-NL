---
uid: Microsoft.Quantum.Intrinsic.Message
title: Bericht functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849363"
---
# <a name="message-function"></a><span data-ttu-id="5c8d7-102">Bericht functie</span><span class="sxs-lookup"><span data-stu-id="5c8d7-102">Message function</span></span>

<span data-ttu-id="5c8d7-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="5c8d7-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="5c8d7-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="5c8d7-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="5c8d7-105">Een bericht wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="5c8d7-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="5c8d7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5c8d7-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="5c8d7-107">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="5c8d7-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="5c8d7-108">Het bericht dat moet worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="5c8d7-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5c8d7-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c8d7-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5c8d7-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5c8d7-110">Remarks</span></span>

<span data-ttu-id="5c8d7-111">Het specifieke gedrag van deze functie is van Simulator afhankelijk, maar in de meeste gevallen wordt het gegeven bericht naar de-console geschreven.</span><span class="sxs-lookup"><span data-stu-id="5c8d7-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>