---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: De functie JWOptimizedGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 8e4c06b9447a2e5838cced876febee03d1af5315
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701816"
---
# <a name="jwoptimizedgeneratorsystem-function"></a><span data-ttu-id="798ba-102">De functie JWOptimizedGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="798ba-102">JWOptimizedGeneratorSystem function</span></span>

<span data-ttu-id="798ba-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="798ba-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="798ba-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="798ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="798ba-105">Hiermee wordt een Hamiltonian die wordt beschreven door omgezet `JWOptimizedHTerms` `GeneratorSystem` in een uitgedrukt in termen van de `GeneratorIndex` Conventie die in dit bestand is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="798ba-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="798ba-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="798ba-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="798ba-107">gegevens: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="798ba-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="798ba-108">Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.</span><span class="sxs-lookup"><span data-stu-id="798ba-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="798ba-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="798ba-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="798ba-110">Representatie van Hamiltonian als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="798ba-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>