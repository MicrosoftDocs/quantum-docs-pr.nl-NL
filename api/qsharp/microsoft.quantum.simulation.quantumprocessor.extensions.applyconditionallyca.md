---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyCA
title: Bewerking ApplyConditionallyCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyCA
qsharp.summary: ''
ms.openlocfilehash: 18db01f8e5e00c2f115b8ffe73c0f8eea275beb0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230239"
---
# <a name="applyconditionallyca-operation"></a>Bewerking ApplyConditionallyCA

Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionallyCA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl + Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl + Adj), nonEqualArg : 'U)) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="measurementresults--__invalidresult__"></a>measurementResults: __ongeldige <Result>__[]




### <a name="resultsvalues--__invalidresult__"></a>resultsValues: __ongeldige <Result>__[]




### <a name="onequalop--t--unit--is-adj--ctl"></a>onEqualOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL




### <a name="equalarg--t"></a>equalArg: 'T




### <a name="onnonequalop--u--unit--is-adj--ctl"></a>onNonEqualOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL




### <a name="nonequalarg--u"></a>nonEqualArg: ' U





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U

