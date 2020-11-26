---
uid: Microsoft.Quantum.Arrays.SequenceI
title: De functie SequenceI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220294"
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