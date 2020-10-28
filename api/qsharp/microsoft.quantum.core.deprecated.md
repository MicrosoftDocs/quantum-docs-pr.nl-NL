---
uid: Microsoft.Quantum.Core.Deprecated
title: Afgeschaft door door de gebruiker gedefinieerd type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: b1fcae9647b2a655d25773386ecffa826515516e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702884"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="8a2af-102">Afgeschaft door door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="8a2af-102">Deprecated user defined type</span></span>

<span data-ttu-id="8a2af-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="8a2af-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="8a2af-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8a2af-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8a2af-105">Een door het compiler herkend kenmerk dat wordt gebruikt om een type of aanroepable te markeren als afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="8a2af-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="8a2af-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="8a2af-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="8a2af-107">Nieuwenaam: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8a2af-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8a2af-108">De volledige naam van het type of aanroepable dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8a2af-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="8a2af-109">Is ingesteld op de lege teken reeks als een type of aanroepable is afgeschaft zonder vervanging.</span><span class="sxs-lookup"><span data-stu-id="8a2af-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>