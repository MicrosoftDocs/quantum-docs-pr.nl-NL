---
uid: Microsoft.Quantum.Logical.NotEqualB
title: De functie NotEqualB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 9f362b9e08f8a798bf7f7d9c323fee6576dccd9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814424"
---
# <a name="notequalb-function"></a>De functie NotEqualB

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bool"></a>a: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De eerste waarde die moet worden vergeleken.


### <a name="b--bool"></a>b: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` is niet gelijk aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let cond = a != b;
let cond = NotEqualB(a, b);
```