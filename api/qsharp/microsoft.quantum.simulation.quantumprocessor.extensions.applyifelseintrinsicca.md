---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicCA
title: Bewerking ApplyIfElseIntrinsicCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 40513e407d4f7a42dffde940cd4b3548d8738a4d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192652"
---
# <a name="applyifelseintrinsicca-operation"></a>Bewerking ApplyIfElseIntrinsicCA

Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyIfElseIntrinsicCA (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl + Adj), onResultOneOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __ongeldig <Result>__




### <a name="onresultzeroop--unit--unit--is-adj--ctl"></a>onResultZeroOp: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL




### <a name="onresultoneop--unit--unit--is-adj--ctl"></a>onResultOneOp: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

