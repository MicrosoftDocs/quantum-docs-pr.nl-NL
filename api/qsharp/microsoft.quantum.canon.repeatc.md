---
uid: Microsoft.Quantum.Canon.RepeatC
title: Bewerking RepeatC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 8dc178374bdc9f8bf9f8aed57b9ae9a56995dec6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703862"
---
# <a name="repeatc-operation"></a>Bewerking RepeatC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Herhaalt een bewerking een bepaald aantal keren.

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a>Invoer

### <a name="op--tinput--unit-ctl"></a>op: ' TInput = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit)

De bewerking die herhaaldelijk moet worden aangeroepen.


### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat moet worden aangeroepen `op` .


### <a name="input--tinput"></a>invoer: ' TInput

De invoer die moet worden door gegeven aan `op` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="tinput"></a>'TInput



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. DrawMany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Micro soft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
- [Micro soft. Quantum. Canon. Repeata](xref:Microsoft.Quantum.Canon.RepeatA)
- [Micro soft. Quantum. Canon. RepeatCA](xref:Microsoft.Quantum.Canon.RepeatCA)