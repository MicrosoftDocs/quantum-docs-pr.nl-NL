---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: Functie _JordanWignerClusterOperatorFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 58b0c7ad2216b1f58b9ea2765494b85fab4e1ff9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703478"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a>Functie _JordanWignerClusterOperatorFunction

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JordanWigner basis.

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a>Invoer

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JordanWigner.



## <a name="output--evolutionunitary"></a>Uitvoer: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)

Een `EvolutionUnitary` representatieve tijd ontwikkeling op basis van de term waarnaar wordt verwezen in generatorIndex.