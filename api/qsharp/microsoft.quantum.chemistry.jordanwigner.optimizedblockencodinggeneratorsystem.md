---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBlockEncodingGeneratorSystem
title: De functie OptimizedBlockEncodingGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: c3e48cb5dde36b694a5b16f25333cf0dad6c0f61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703149"
---
# <a name="optimizedblockencodinggeneratorsystem-function"></a>De functie OptimizedBlockEncodingGeneratorSystem

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Hamiltonian die wordt beschreven door `JWOptimizedHTerms` naar een `GeneratorSystem` uitgedrukt in termen van de Pauli, geconverteerd `GeneratorIndex` .

```qsharp
function OptimizedBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="data--jwoptimizedhterms"></a>gegevens: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)

Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.



## <a name="output--optimizedbegeneratorsystem"></a>Uitvoer: [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)

Representatie van Hamiltonian als `GeneratorSystem` .