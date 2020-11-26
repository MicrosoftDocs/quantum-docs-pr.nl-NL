---
uid: Microsoft.Quantum.Core.Deprecated
title: Afgeschaft door door de gebruiker gedefinieerd type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 122cbc113a68cec107558d68a6fb145cf6bbd9db
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224085"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="d58cc-102">Afgeschaft door door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="d58cc-102">Deprecated user defined type</span></span>

<span data-ttu-id="d58cc-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="d58cc-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="d58cc-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d58cc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d58cc-105">Een door het compiler herkend kenmerk dat wordt gebruikt om een type of aanroepable te markeren als afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="d58cc-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="d58cc-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="d58cc-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="d58cc-107">Nieuwenaam: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d58cc-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d58cc-108">De volledige naam van het type of aanroepable dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d58cc-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="d58cc-109">Is ingesteld op de lege teken reeks als een type of aanroepable is afgeschaft zonder vervanging.</span><span class="sxs-lookup"><span data-stu-id="d58cc-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>