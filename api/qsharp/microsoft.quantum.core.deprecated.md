---
uid: Microsoft.Quantum.Core.Deprecated
title: Afgeschaft door door de gebruiker gedefinieerd type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 1a32d98f5d034c2673d42301b45379da1302ca7f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832088"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="c9d3a-102">Afgeschaft door door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="c9d3a-102">Deprecated user defined type</span></span>

<span data-ttu-id="c9d3a-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="c9d3a-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="c9d3a-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c9d3a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c9d3a-105">Een door het compiler herkend kenmerk dat wordt gebruikt om een type of aanroepable te markeren als afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="c9d3a-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="c9d3a-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="c9d3a-107">Nieuwenaam: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c9d3a-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c9d3a-108">De volledige naam van het type of aanroepable dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="c9d3a-109">Is ingesteld op de lege teken reeks als een type of aanroepable is afgeschaft zonder vervanging.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>