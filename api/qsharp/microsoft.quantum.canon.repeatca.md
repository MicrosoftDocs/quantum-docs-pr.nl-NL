---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Bewerking RepeatCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852214"
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



## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. DrawMany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Micro soft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
- [Micro soft. Quantum. Canon. Repeata](xref:Microsoft.Quantum.Canon.RepeatA)
- [Micro soft. Quantum. Canon. RepeatC](xref:Microsoft.Quantum.Canon.RepeatC)