---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyCA
title: Bewerking ApplyConditionallyCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyCA
qsharp.summary: ''
ms.openlocfilehash: e456ed5d8f7f17a914401473948c89c020174903
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706645"
---
# <a name="applyconditionallyca-operation"></a>Bewerking ApplyConditionallyCA

Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Pakket [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyCA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl + Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl + Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>Invoer

### <a name="measurementresults--__invalidresult__"></a>measurementResults: __ongeldige <Result>__ []




### <a name="resultsvalues--__invalidresult__"></a>resultsValues: __ongeldige <Result>__ []




### <a name="onequalop--t--unit-ctl--adj"></a>onEqualOp: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) en correctie




### <a name="equalarg--t"></a>equalArg: 'T




### <a name="onnonequalop--u--unit-ctl--adj"></a>onNonEqualOp: ' U = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie




### <a name="nonequalarg--u"></a>nonEqualArg: ' U





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U

