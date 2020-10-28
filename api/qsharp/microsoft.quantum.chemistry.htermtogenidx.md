---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: De functie HTermToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703551"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="f62f5-102">De functie HTermToGenIdx</span><span class="sxs-lookup"><span data-stu-id="f62f5-102">HTermToGenIdx function</span></span>

<span data-ttu-id="f62f5-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f62f5-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="f62f5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f62f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f62f5-105">Hiermee wordt een Hamiltonian-term in `HTerm` een gegevens indeling geconverteerd naar een GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="f62f5-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="f62f5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f62f5-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="f62f5-107">term: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="f62f5-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="f62f5-108">Invoer gegevens in de `HTerm` indeling.</span><span class="sxs-lookup"><span data-stu-id="f62f5-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="f62f5-109">termType: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f62f5-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f62f5-110">Aanvullende informatie toegevoegd aan GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="f62f5-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="f62f5-111">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="f62f5-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="f62f5-112">Een GeneratorIndex die een Hamiltonian-term vertegenwoordigt die wordt vertegenwoordigd door `term` , samen met aanvullende informatie toegevoegd door `termType` .</span><span class="sxs-lookup"><span data-stu-id="f62f5-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>