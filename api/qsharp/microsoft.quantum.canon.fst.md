---
uid: Microsoft.Quantum.Canon.Fst
title: De functie FST
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840523"
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