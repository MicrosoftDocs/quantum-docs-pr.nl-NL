---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: De functie HTermsToGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: dbe0718fa3b5439a2987d455fdad73731c988678
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216010"
---
# <a name="htermstogenidx-function"></a>De functie HTermsToGenIdx

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Converteert een index naar een Hamiltonian-term in `HTerm[]` een gegevens indeling naar een GeneratorIndex.

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Invoer

### <a name="data--hterm"></a>gegevens: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Invoer gegevens in de `HTerm[]` indeling.


### <a name="termtype--int"></a>termType: [int](xref:microsoft.quantum.lang-ref.int)[]

Aanvullende informatie toegevoegd aan GeneratorIndex.


### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Index naar een periode van de Hamiltonian



## <a name="output--generatorindex"></a>Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een GeneratorIndex die een Hamiltonian-term vertegenwoordigt die wordt vertegenwoordigd door `data[idx]` , samen met aanvullende informatie toegevoegd door `termType` .