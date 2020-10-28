---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: De functie HTermToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703551"
---
# <a name="htermtogenidx-function"></a>De functie HTermToGenIdx

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Hamiltonian-term in `HTerm` een gegevens indeling geconverteerd naar een GeneratorIndex.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Invoer

### <a name="term--hterm"></a>term: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)

Invoer gegevens in de `HTerm` indeling.


### <a name="termtype--int"></a>termType: [int](xref:microsoft.quantum.lang-ref.int)[]

Aanvullende informatie toegevoegd aan GeneratorIndex.



## <a name="output--generatorindex"></a>Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een GeneratorIndex die een Hamiltonian-term vertegenwoordigt die wordt vertegenwoordigd door `term` , samen met aanvullende informatie toegevoegd door `termType` .