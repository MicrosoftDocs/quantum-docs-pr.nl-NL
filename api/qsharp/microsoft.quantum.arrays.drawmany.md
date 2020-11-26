---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Bewerking DrawMany
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209992"
---
# <a name="drawmany-operation"></a>Bewerking DrawMany

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking herhaald voor een bepaald aantal steek proeven, waarbij de uitvoer ervan in een matrix wordt verzameld.

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a>Invoer

### <a name="op--tinput--toutput"></a>op: ' TInput => ' TOutput 

De bewerking die herhaaldelijk moet worden aangeroepen.


### <a name="nsamples--int"></a>nSamples: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal voor beelden van aanroepen `op` om te verzamelen.


### <a name="input--tinput"></a>invoer: ' TInput

De invoer die moet worden door gegeven aan `op` .



## <a name="output--toutput"></a>Uitvoer: ' TOutput []



## <a name="type-parameters"></a>Type parameters

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>'TOutput



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)