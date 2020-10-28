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
# <a name="deprecated-user-defined-type"></a>Afgeschaft door door de gebruiker gedefinieerd type

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket [](https://nuget.org/packages/)


Een door het compiler herkend kenmerk dat wordt gebruikt om een type of aanroepable te markeren als afgeschaft.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Benoemde items

### <a name="newname--string"></a>Nieuwenaam: [teken reeks](xref:microsoft.quantum.lang-ref.string)

De volledige naam van het type of aanroepable dat moet worden gebruikt.
Is ingesteld op de lege teken reeks als een type of aanroepable is afgeschaft zonder vervanging.