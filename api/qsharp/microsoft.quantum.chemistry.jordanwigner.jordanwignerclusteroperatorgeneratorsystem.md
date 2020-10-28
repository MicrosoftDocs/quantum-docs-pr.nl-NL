---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerClusterOperatorGeneratorSystem
title: De functie JordanWignerClusterOperatorGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerClusterOperatorGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: c75dcd655dafb7048f61f4b07b852cc5f437275d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703220"
---
# <a name="jordanwignerclusteroperatorgeneratorsystem-function"></a>De functie JordanWignerClusterOperatorGeneratorSystem

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Hamiltonian die wordt beschreven door omgezet `JWOptimizedHTerms` `GeneratorSystem` in een uitgedrukt in termen van de `GeneratorIndex` Conventie die in dit bestand is gedefinieerd.

```qsharp
function JordanWignerClusterOperatorGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="data--jordanwignerinputstate"></a>gegevens: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]

Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Representatie van Hamiltonian als `GeneratorSystem` .