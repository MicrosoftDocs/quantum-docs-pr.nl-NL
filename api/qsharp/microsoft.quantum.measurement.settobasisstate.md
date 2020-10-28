---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Bewerking SetToBasisState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708940"
---
# <a name="settobasisstate-operation"></a>Bewerking SetToBasisState

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Qubit ingesteld op basis van de status van de berekening door de Qubit te meten en zo nodig een bit te spie gelen.

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="desired--__invalidresult__"></a>gewenst: __ongeldig <Result>__

De basis status waarop de Qubit moet worden ingesteld.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De Qubit waarvan de status moet worden ingesteld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Als een onvariante van deze bewerking, `M(q)` wordt direct na `SetToBasisState(result, q)` geretourneerd `result` .