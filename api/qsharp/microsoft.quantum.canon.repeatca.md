---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Bewerking RepeatCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205402"
---
# <a name="repeatca-operation"></a>Bewerking RepeatCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Herhaalt een bewerking een bepaald aantal keren.

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="op--tinput--unit--is-adj--ctl"></a>op: ' TInput => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

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
- [Micro soft. Quantum. Canon. RepeatC](xref:Microsoft.Quantum.Canon.RepeatC)