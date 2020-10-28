---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706140"
---
# <a name="constantarray-function"></a>De functie ConstantArray

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

