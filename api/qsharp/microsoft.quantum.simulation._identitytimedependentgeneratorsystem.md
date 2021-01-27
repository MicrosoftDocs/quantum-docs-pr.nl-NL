---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Functie _IdentityTimeDependentGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857986"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="120e7-102">Functie _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="120e7-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="120e7-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="120e7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="120e7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="120e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="120e7-105">Retourneert een generator systeem dat consistent is met de Hamiltonian `H(s) = 0` , waarbij `s` een schema parameter is.</span><span class="sxs-lookup"><span data-stu-id="120e7-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="120e7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="120e7-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="120e7-107">planning: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="120e7-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="120e7-108">Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.canon.timedependentgeneratorsystem> gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="120e7-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="120e7-109">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="120e7-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="120e7-110">Een generator systeem dat de ontwikkeling weergeeft van de Hamiltonian $H (s) = $0 voor alle $s $.</span><span class="sxs-lookup"><span data-stu-id="120e7-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>