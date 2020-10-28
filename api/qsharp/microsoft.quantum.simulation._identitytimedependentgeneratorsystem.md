---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Functie _IdentityTimeDependentGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701775"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Functie _IdentityTimeDependentGeneratorSystem

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Retourneert een generator systeem dat consistent is met de Hamiltonian `H(s) = 0` , waarbij `s` een schema parameter is.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="schedule--double"></a>planning: [dubbel](xref:microsoft.quantum.lang-ref.double)

Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.canon.timedependentgeneratorsystem> gebruiker gedefinieerde type.



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een generator systeem dat de ontwikkeling weergeeft van de Hamiltonian $H (s) = $0 voor alle $s $.