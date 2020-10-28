---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: De functie _PQTermToPauliGenIdx_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 1f9567f327b5afc3054acbf1a615b44a54453004
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703341"
---
# <a name="_pqtermtopauligenidx_-function"></a>De functie _PQTermToPauliGenIdx_

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een GeneratorIndex die een PQ-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a>Invoer

### <a name="term--generatorindex"></a>term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` een PQ-term vertegenwoordigt.



## <a name="output--generatorindex"></a>Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]

' GeneratorIndex [] ' expressing PQ-term als Pauli-voor waarden.