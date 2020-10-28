---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliMajIdx_
title: De functie _V0123TermToPauliMajIdx_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 7295b510de2621698d48d40ac28e234d0c8915eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703275"
---
# <a name="_v0123termtopaulimajidx_-function"></a>De functie _V0123TermToPauliMajIdx_

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een GeneratorIndex die een PQRS-term beschrijft, geconverteerd naar een expressie ' GeneratorIndex [] ' in termen van PAULIS

```qsharp
function _V0123TermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex[]
```


## <a name="input"></a>Invoer

### <a name="term--generatorindex"></a>term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` een PQRS-term vertegenwoordigt.



## <a name="output--optimizedbetermindex"></a>Uitvoer: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)[]

' GeneratorIndex [] ' expressing PQRS-term als Pauli-voor waarden.