---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: De functie HTermsToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703562"
---
# <a name="htermstogenidx-function"></a>De functie HTermsToGenIdx

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket [](https://nuget.org/packages/)


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