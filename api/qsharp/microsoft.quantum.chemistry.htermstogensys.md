---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: De functie HTermsToGenSys
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703556"
---
# <a name="htermstogensys-function"></a><span data-ttu-id="4bcf6-102">De functie HTermsToGenSys</span><span class="sxs-lookup"><span data-stu-id="4bcf6-102">HTermsToGenSys function</span></span>

<span data-ttu-id="4bcf6-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="4bcf6-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="4bcf6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4bcf6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4bcf6-105">Hiermee wordt een Hamiltonian in `HTerm[]` de gegevens indeling geconverteerd naar een GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-105">Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.</span></span>

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="4bcf6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4bcf6-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="4bcf6-107">gegevens: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="4bcf6-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="4bcf6-108">Invoer gegevens in de `HTerm[]` indeling.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="4bcf6-109">termType: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4bcf6-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4bcf6-110">Aanvullende informatie toegevoegd aan GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="4bcf6-111">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="4bcf6-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="4bcf6-112">Een GeneratorSystem die een Hamiltonian vertegenwoordigt die wordt vertegenwoordigd door de invoer `data` .</span><span class="sxs-lookup"><span data-stu-id="4bcf6-112">A GeneratorSystem representing a Hamiltonian represented by the input `data`.</span></span>