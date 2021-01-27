---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: De functie IdentityGeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: b389ca1e0737463e6ccd5ce885b849c6b32d65d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844344"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="93ef1-102">De functie IdentityGeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="93ef1-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="93ef1-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="93ef1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="93ef1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93ef1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93ef1-105">Retourneert een generator index die consistent is met de Hamiltonian nul, `H = 0` , die overeenkomt met de bewerking voor identiteits ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="93ef1-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="93ef1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="93ef1-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="93ef1-107">idxTerm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="93ef1-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="93ef1-108">Deze invoer wordt genegeerd en wordt gedefinieerd voor consistentie met het door de <xref:microsoft.quantum.simulation.generatorsystem> gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="93ef1-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="93ef1-109">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="93ef1-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="93ef1-110">Een generator index die de ontwikkeling weergeeft onder het Hamiltonian-$H = $0.</span><span class="sxs-lookup"><span data-stu-id="93ef1-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>