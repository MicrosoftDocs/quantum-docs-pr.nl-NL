---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Bewerking DrawMany
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706109"
---
# <a name="drawmany-operation"></a>Bewerking DrawMany

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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