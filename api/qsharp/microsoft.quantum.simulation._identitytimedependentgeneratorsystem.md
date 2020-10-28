---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Functie _IdentityTimeDependentGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701775"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="34799-102">Functie _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="34799-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="34799-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="34799-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="34799-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34799-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34799-105">Retourneert een generator systeem dat consistent is met de Hamiltonian `H(s) = 0` , waarbij `s` een schema parameter is.</span><span class="sxs-lookup"><span data-stu-id="34799-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="34799-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="34799-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="34799-107">planning: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="34799-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="34799-108">Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.canon.timedependentgeneratorsystem> gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="34799-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="34799-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="34799-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="34799-110">Een generator systeem dat de ontwikkeling weergeeft van de Hamiltonian $H (s) = $0 voor alle $s $.</span><span class="sxs-lookup"><span data-stu-id="34799-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>