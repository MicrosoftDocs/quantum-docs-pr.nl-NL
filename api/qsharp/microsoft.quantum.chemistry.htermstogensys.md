---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: De functie HTermsToGenSys
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 3d5963b8751a22d7116d6c1cf094d89e1d6b556f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851767"
---
# <a name="htermstogensys-function"></a><span data-ttu-id="192ca-102">De functie HTermsToGenSys</span><span class="sxs-lookup"><span data-stu-id="192ca-102">HTermsToGenSys function</span></span>

<span data-ttu-id="192ca-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="192ca-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="192ca-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="192ca-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="192ca-105">Hiermee wordt een Hamiltonian in `HTerm[]` de gegevens indeling geconverteerd naar een GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="192ca-105">Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.</span></span>

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="192ca-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="192ca-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="192ca-107">gegevens: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="192ca-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="192ca-108">Invoer gegevens in de `HTerm[]` indeling.</span><span class="sxs-lookup"><span data-stu-id="192ca-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="192ca-109">termType: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="192ca-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="192ca-110">Aanvullende informatie toegevoegd aan GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="192ca-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="192ca-111">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="192ca-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="192ca-112">Een GeneratorSystem die een Hamiltonian vertegenwoordigt die wordt vertegenwoordigd door de invoer `data` .</span><span class="sxs-lookup"><span data-stu-id="192ca-112">A GeneratorSystem representing a Hamiltonian represented by the input `data`.</span></span>