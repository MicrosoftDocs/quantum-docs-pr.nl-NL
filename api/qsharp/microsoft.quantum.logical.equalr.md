---
uid: Microsoft.Quantum.Logical.EqualR
title: Functie EQUAL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 9ce29f2868f092001a3dca23a2913a3963ac70fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815986"
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

```qsharp
let cond = a == b;
let cond = EqualR(a, b);
```