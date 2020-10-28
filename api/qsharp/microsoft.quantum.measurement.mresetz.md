---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Bewerking MResetZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 9f084b03504deea9fcf25e4c797c4bde3c97a995
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701931"
---
# <a name="mresetz-operation"></a>Bewerking MResetZ

Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)

Pakket [](https://nuget.org/packages/)


Hiermee wordt één Qubit in de Z-basis gemeten en teruggezet naar een vaste begin status na de meting.

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a>Beschrijving

Voert een meting met één Qubit uit in de $Z $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.

## <a name="input"></a>Invoer

### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eén Qubit die moet worden gemeten.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

Het resultaat van het meten van `target` de Pauli-$Z $ soort_jaar.