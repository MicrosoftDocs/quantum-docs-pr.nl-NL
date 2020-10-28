---
uid: Microsoft.Quantum.Measurement.MResetY
title: Bewerking MResetY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709084"
---
# <a name="mresety-operation"></a>Bewerking MResetY

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket [](https://nuget.org/packages/)


Hiermee wordt één Qubit in de Y-eenheid gemeten en teruggezet naar een vaste begin status na de meting.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>Beschrijving

Voert een meting met één Qubit uit in de $Y $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.

## <a name="input"></a>Invoer

### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eén Qubit die moet worden gemeten.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

Het resultaat van het meten van `target` de Pauli-$Y $ soort_jaar.