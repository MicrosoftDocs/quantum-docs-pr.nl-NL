---
uid: Microsoft.Quantum.Canon.Fst
title: De functie FST
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206932"
---
# <a name="fst-function"></a>De functie FST

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Het eerste element wordt geretourneerd door een paar.

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a>Invoer

### <a name="pair--tu"></a>paar: ('T, ' U ')

Een tuple met twee elementen.



## <a name="output--t"></a>Uitvoer: 'T

Het eerste element van `pair` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste lid van het paar.
### <a name="u"></a>' U

Het type van het tweede lid van het paar.