---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerClusterOperatorGeneratorSystem
title: De functie JordanWignerClusterOperatorGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerClusterOperatorGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: e6deca3c8261c7730e9b208d9f834ad0db101fd3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214803"
---
# <a name="jordanwignerclusteroperatorgeneratorsystem-function"></a><span data-ttu-id="842d2-102">De functie JordanWignerClusterOperatorGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="842d2-102">JordanWignerClusterOperatorGeneratorSystem function</span></span>

<span data-ttu-id="842d2-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="842d2-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="842d2-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="842d2-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="842d2-105">Hiermee wordt een Hamiltonian die wordt beschreven door omgezet `JWOptimizedHTerms` `GeneratorSystem` in een uitgedrukt in termen van de `GeneratorIndex` Conventie die in dit bestand is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="842d2-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerClusterOperatorGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="842d2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="842d2-106">Input</span></span>

### <a name="data--jordanwignerinputstate"></a><span data-ttu-id="842d2-107">gegevens: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="842d2-107">data : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="842d2-108">Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.</span><span class="sxs-lookup"><span data-stu-id="842d2-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="842d2-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="842d2-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="842d2-110">Representatie van Hamiltonian als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="842d2-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>