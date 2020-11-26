---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210060"
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

