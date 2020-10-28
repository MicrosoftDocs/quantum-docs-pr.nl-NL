---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: De functie HTermsToGenSys
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703556"
---
# <a name="htermstogensys-function"></a>De functie HTermsToGenSys

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Hamiltonian in `HTerm[]` de gegevens indeling geconverteerd naar een GeneratorSystem.

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="data--hterm"></a>gegevens: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Invoer gegevens in de `HTerm[]` indeling.


### <a name="termtype--int"></a>termType: [int](xref:microsoft.quantum.lang-ref.int)[]

Aanvullende informatie toegevoegd aan GeneratorIndex.



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een GeneratorSystem die een Hamiltonian vertegenwoordigt die wordt vertegenwoordigd door de invoer `data` .