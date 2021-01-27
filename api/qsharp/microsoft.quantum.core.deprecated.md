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
# <a name="deprecated-user-defined-type"></a>Afgeschaft door door de gebruiker gedefinieerd type

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Een door het compiler herkend kenmerk dat wordt gebruikt om een type of aanroepable te markeren als afgeschaft.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Benoemde items

### <a name="newname--string"></a>Nieuwenaam: [teken reeks](xref:microsoft.quantum.lang-ref.string)

De volledige naam van het type of aanroepable dat moet worden gebruikt.
Is ingesteld op de lege teken reeks als een type of aanroepable is afgeschaft zonder vervanging.