---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Bewerking AllowAtMostNCallsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702794"
---
# <a name="allowatmostncallsca-operation"></a>Bewerking AllowAtMostNCallsCA

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Tussen een aanroep van deze bewerking en de adjoint wordt bevestigd dat een bepaalde bewerking Maxi maal een bepaald aantal keer wordt aangeroepen.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Het maximum aantal keer dat `op` kan worden aangeroepen.


### <a name="op--tinput--toutput-adj--ctl"></a>op: ' TInput => ' TOutput ADJ + CTL

Een bewerking waarvan de aanroepen moeten worden beperkt.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>'TOutput



## <a name="remarks"></a>Opmerkingen

Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.