---
uid: Microsoft.Quantum.Arrays.SequenceI
title: De functie SequenceI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705796"
---
# <a name="sequencei-function"></a>De functie SequenceI

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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