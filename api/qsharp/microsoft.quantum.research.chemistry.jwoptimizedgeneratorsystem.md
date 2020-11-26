---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: De functie JWOptimizedGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 321b58ba4a458ad53579d2480258a92ba48de169
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225700"
---
# <a name="jwoptimizedgeneratorsystem-function"></a><span data-ttu-id="8a3d4-102">De functie JWOptimizedGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="8a3d4-102">JWOptimizedGeneratorSystem function</span></span>

<span data-ttu-id="8a3d4-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8a3d4-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="8a3d4-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8a3d4-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="8a3d4-105">Hiermee wordt een Hamiltonian die wordt beschreven door omgezet `JWOptimizedHTerms` `GeneratorSystem` in een uitgedrukt in termen van de `GeneratorIndex` Conventie die in dit bestand is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="8a3d4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8a3d4-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="8a3d4-107">gegevens: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="8a3d4-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="8a3d4-108">Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="8a3d4-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8a3d4-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="8a3d4-110">Representatie van Hamiltonian als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="8a3d4-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>