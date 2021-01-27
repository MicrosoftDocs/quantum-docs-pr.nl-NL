---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846231"
---
# <a name="constantarray-function"></a>De functie ConstantArray

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt een matrix met de opgegeven lengte en alle elementen die gelijk zijn aan de opgegeven waarde.

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="length--int"></a>lengte: [int](xref:microsoft.quantum.lang-ref.int)

Lengte van de nieuwe matrix.


### <a name="value--t"></a>waarde: 'T

De waarde van elk element van de nieuwe matrix.



## <a name="output--t"></a>Uitvoer: ' []

Een nieuwe matrix met lengte `length` , zodat elk element is `value` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="example"></a>Voorbeeld

Met de volgende code wordt een matrix van drie Booleaanse waarden gemaakt die gelijk zijn aan `true` :

```qsharp
let array = ConstantArray(3, true);
```