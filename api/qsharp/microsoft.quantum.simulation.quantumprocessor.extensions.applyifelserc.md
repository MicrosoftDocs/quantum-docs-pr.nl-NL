---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Bewerking ApplyIfElseRC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 33b3adfca87410480108eafd090632006117f7b2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192635"
---
# <a name="applyifelserc-operation"></a>Bewerking ApplyIfElseRC

Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit is Ctl
```


## <a name="input"></a>Invoer

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __ongeldig <Result>__




### <a name="onresultzeroop--t--unit--is-ctl"></a>onResultZeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL




### <a name="zeroarg--t"></a>zeroArg: 'T




### <a name="onresultoneop--u--unit--is-ctl"></a>onResultOneOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL




### <a name="onearg--u"></a>oneArg: ' U





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U

