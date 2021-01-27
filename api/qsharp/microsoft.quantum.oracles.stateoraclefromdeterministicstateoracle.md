---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: De functie StateOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842509"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="fdb4a-102">De functie StateOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="fdb4a-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="fdb4a-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="fdb4a-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="fdb4a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdb4a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdb4a-105">Converteert een Oracle van het type `DeterministicStateOracle` naar `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="fdb4a-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="fdb4a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fdb4a-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="fdb4a-107">deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="fdb4a-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="fdb4a-108">Een status voorbereiding Oracle $A $ van type `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="fdb4a-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="fdb4a-109">Uitvoer: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="fdb4a-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="fdb4a-110">Dezelfde status voorbereiding Oracle $A $, maar nu van type `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="fdb4a-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="fdb4a-111">Houd er rekening mee dat de vlag index in dit `StateOracle` een dummy variabele is en geen effect heeft.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdb4a-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fdb4a-112">See Also</span></span>

- [<span data-ttu-id="fdb4a-113">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="fdb4a-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="fdb4a-114">Micro soft. Quantum. Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="fdb4a-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)