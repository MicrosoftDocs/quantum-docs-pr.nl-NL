---
uid: Microsoft.Quantum.Arrays.SequenceI
title: De functie SequenceI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3cf09e48cce1aeb1aac837465ee3a5e06adf5169
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850995"
---
# <a name="sequencei-function"></a>De functie SequenceI

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een matrix van gehele getallen ophalen binnen een bepaalde interval.

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a>Invoer

### <a name="from--int"></a>van: [int](xref:microsoft.quantum.lang-ref.int)

Een inclusieve start index van het interval.


### <a name="to--int"></a>naar: [int](xref:microsoft.quantum.lang-ref.int)

Een inclusieve eind index van het interval dat niet kleiner is dan `from` .



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .

## <a name="example"></a>Voorbeeld

```qsharp
let arr1 = SequenceI(0, 3); // [0, 1, 2, 3]
let arr2 = SequenceI(23, 29); // [23, 24, 25, 26, 27, 28, 29]
let arr3 = SequenceI(-5, -2); // [-5, -4, -3, -2]

let numbers = SequenceI(0, _); // function to create sequence from 0 to `to`
let naturals = SequenceI(1, _); // function to create sequence from 1 to `to`
```