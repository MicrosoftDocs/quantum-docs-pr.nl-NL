---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Bewerking ApplyBlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707848"
---
# <a name="applyblockencodingbylcu-operation"></a>Bewerking ApplyBlockEncodingByLCU

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Implementatie van `BlockEncodingByLCU` .

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a>Invoer

### <a name="statepreparation--t--unit-adj--ctl"></a>statePreparation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL




### <a name="selector--ts--unit-adj--ctl"></a>kiezer: ('T) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL




### <a name="auxiliary--t"></a>hulp: 'T




### <a name="system--s"></a>systeem:





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="s"></a>Maatschappij

