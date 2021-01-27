---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: De functie HTermsToGenIdx
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 84dc132528f8fd1c45fb2f7345111a05626ee686
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839637"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="452a6-102">De functie HTermsToGenIdx</span><span class="sxs-lookup"><span data-stu-id="452a6-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="452a6-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="452a6-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="452a6-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="452a6-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="452a6-105">Converteert een index naar een Hamiltonian-term in `HTerm[]` een gegevens indeling naar een GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="452a6-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="452a6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="452a6-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="452a6-107">gegevens: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="452a6-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="452a6-108">Invoer gegevens in de `HTerm[]` indeling.</span><span class="sxs-lookup"><span data-stu-id="452a6-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="452a6-109">termType: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="452a6-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="452a6-110">Aanvullende informatie toegevoegd aan GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="452a6-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="452a6-111">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="452a6-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="452a6-112">Index naar een periode van de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="452a6-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="452a6-113">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="452a6-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="452a6-114">Een GeneratorIndex die een Hamiltonian-term vertegenwoordigt die wordt vertegenwoordigd door `data[idx]` , samen met aanvullende informatie toegevoegd door `termType` .</span><span class="sxs-lookup"><span data-stu-id="452a6-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>