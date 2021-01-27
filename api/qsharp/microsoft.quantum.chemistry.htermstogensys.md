---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: De functie HTermsToGenSys
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 3d5963b8751a22d7116d6c1cf094d89e1d6b556f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851767"
---
# <a name="htermstogensys-function"></a>De functie HTermsToGenSys

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


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