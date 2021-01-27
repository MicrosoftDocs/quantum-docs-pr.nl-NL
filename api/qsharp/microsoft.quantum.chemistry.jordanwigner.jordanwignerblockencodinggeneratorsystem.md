---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerBlockEncodingGeneratorSystem
title: De functie JordanWignerBlockEncodingGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: cffbb1e2d9b6566bf6c3da642e4479968f774ca3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839036"
---
# <a name="jordanwignerblockencodinggeneratorsystem-function"></a><span data-ttu-id="eca52-102">De functie JordanWignerBlockEncodingGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="eca52-102">JordanWignerBlockEncodingGeneratorSystem function</span></span>

<span data-ttu-id="eca52-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="eca52-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="eca52-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="eca52-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="eca52-105">Hiermee wordt een Hamiltonian die wordt beschreven door `JWOptimizedHTerms` naar een `GeneratorSystem` uitgedrukt in termen van de Pauli, geconverteerd `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="eca52-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.</span></span>

```qsharp
function JordanWignerBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="eca52-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="eca52-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="eca52-107">gegevens: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="eca52-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="eca52-108">Beschrijving van de Hamiltonian in de `JWOptimizedHTerms` indeling.</span><span class="sxs-lookup"><span data-stu-id="eca52-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="eca52-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="eca52-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="eca52-110">Representatie van Hamiltonian als `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="eca52-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>