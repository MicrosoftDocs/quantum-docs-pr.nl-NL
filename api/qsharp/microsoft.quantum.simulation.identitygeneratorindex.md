---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: De functie IdentityGeneratorIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708881"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="1474b-102">De functie IdentityGeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="1474b-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="1474b-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1474b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1474b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1474b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1474b-105">Retourneert een generator index die consistent is met de Hamiltonian nul, `H = 0` , die overeenkomt met de bewerking voor identiteits ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="1474b-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="1474b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1474b-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="1474b-107">idxTerm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1474b-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1474b-108">Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.simulation.generatorsystem> gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="1474b-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="1474b-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="1474b-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="1474b-110">Een generator index die de ontwikkeling weergeeft onder het Hamiltonian-$H = $0.</span><span class="sxs-lookup"><span data-stu-id="1474b-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>