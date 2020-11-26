---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerGeneratorSystem
title: De functie JordanWignerGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 0f6719cfac1c50cd55da30e57b0b5c5214813f24
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214718"
---
# <a name="jordanwignergeneratorsystem-function"></a><span data-ttu-id="d109b-102">De functie JordanWignerGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="d109b-102">JordanWignerGeneratorSystem function</span></span>

<span data-ttu-id="d109b-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d109b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d109b-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d109b-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d109b-105">Hiermee wordt een Hamiltonian die wordt beschreven door omgezet `JWOptimizedHTerms` `GeneratorSystem` in een uitgedrukt in termen van de `GeneratorIndex` Conventie die in dit bestand is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d109b-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="d109b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d109b-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="d109b-107">gegevens: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="d109b-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="d109b-108">Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.</span><span class="sxs-lookup"><span data-stu-id="d109b-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="d109b-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="d109b-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="d109b-110">Representatie van Hamiltonian als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="d109b-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>