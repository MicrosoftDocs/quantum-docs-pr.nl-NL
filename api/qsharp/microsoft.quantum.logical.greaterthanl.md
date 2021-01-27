---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: De functie GreaterThanL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 2247c1c1ae8b37b59e87c0c68b06fd1094c9003b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849205"
---
# <a name="greaterthanl-function"></a>De functie GreaterThanL

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als een getal groter is dan een ander getal.

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De eerste waarde die moet worden vergeleken.


### <a name="b--bigint"></a>b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als dit `a` strikt groter is dan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let cond = a > b;
let cond = GreaterThanL(a, b);
```