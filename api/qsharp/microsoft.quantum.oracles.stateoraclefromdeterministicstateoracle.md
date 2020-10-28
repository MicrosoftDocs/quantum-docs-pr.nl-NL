---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: De functie StateOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708743"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="be6a4-102">De functie StateOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="be6a4-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="be6a4-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="be6a4-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="be6a4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="be6a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="be6a4-105">Converteert een Oracle van het type `DeterministicStateOracle` naar `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="be6a4-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="be6a4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="be6a4-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="be6a4-107">deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="be6a4-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="be6a4-108">Een status voorbereiding Oracle $A $ van type `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="be6a4-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="be6a4-109">Uitvoer: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="be6a4-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="be6a4-110">Dezelfde status voorbereiding Oracle $A $, maar nu van type `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="be6a4-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="be6a4-111">Houd er rekening mee dat de vlag index in dit `StateOracle` een dummy variabele is en geen effect heeft.</span><span class="sxs-lookup"><span data-stu-id="be6a4-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="be6a4-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="be6a4-112">See Also</span></span>

- [<span data-ttu-id="be6a4-113">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="be6a4-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="be6a4-114">Micro soft. Quantum. Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="be6a4-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)