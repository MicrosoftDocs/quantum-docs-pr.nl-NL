---
uid: Microsoft.Quantum.Logical.NotEqualR
title: De functie NotEqualR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197191"
---
# <a name="notequalr-function"></a>De functie NotEqualR

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--__invalidresult__"></a>a: __ongeldig <Result>__

De eerste waarde die moet worden vergeleken.


### <a name="b--__invalidresult__"></a>b: __ongeldig <Result>__

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` is niet gelijk aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```