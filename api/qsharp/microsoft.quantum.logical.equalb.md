---
uid: Microsoft.Quantum.Logical.EqualB
title: De functie EqualB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 91ab51180018a9b95a2f9010477c0a24f3a54617
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707052"
---
# <a name="equalb-function"></a>De functie EqualB

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert waar als en alleen als twee invoer waarden gelijk zijn.

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bool"></a>a: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De eerste waarde die moet worden vergeleken.


### <a name="b--bool"></a>b: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` is gelijk aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```