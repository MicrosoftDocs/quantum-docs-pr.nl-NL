---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Functie _IdentityTimeDependentGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857986"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Functie _IdentityTimeDependentGeneratorSystem

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een generator systeem dat consistent is met de Hamiltonian `H(s) = 0` , waarbij `s` een schema parameter is.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="schedule--double"></a>planning: [dubbel](xref:microsoft.quantum.lang-ref.double)

Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.canon.timedependentgeneratorsystem> gebruiker gedefinieerde type.



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een generator systeem dat de ontwikkeling weergeeft van de Hamiltonian $H (s) = $0 voor alle $s $.