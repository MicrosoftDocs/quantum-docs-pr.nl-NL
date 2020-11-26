---
uid: Microsoft.Quantum.Logical.EqualR
title: Functie EQUAL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d68b2f1a26bf318400d3c88b37d9aabcc38cbdfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198003"
---
# <a name="equalr-function"></a>Functie EQUAL

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als twee invoer waarden gelijk zijn.

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--__invalidresult__"></a>a: __ongeldig <Result>__

De eerste waarde die moet worden vergeleken.


### <a name="b--__invalidresult__"></a>b: __ongeldig <Result>__

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` is gelijk aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```