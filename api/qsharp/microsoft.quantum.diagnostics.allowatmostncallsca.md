---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Bewerking AllowAtMostNCallsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202563"
---
# <a name="allowatmostncallsca-operation"></a>Bewerking AllowAtMostNCallsCA

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Tussen een aanroep van deze bewerking en de adjoint wordt bevestigd dat een bepaalde bewerking Maxi maal een bepaald aantal keer wordt aangeroepen.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Het maximum aantal keer dat `op` kan worden aangeroepen.


### <a name="op--tinput--toutput--is-adj--ctl"></a>op: ' TInput => ' TOutput is ADJ en CTL

Een bewerking waarvan de aanroepen moeten worden beperkt.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>'TOutput



## <a name="remarks"></a>Opmerkingen

Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.