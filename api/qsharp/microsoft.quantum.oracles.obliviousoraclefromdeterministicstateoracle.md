---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: De functie ObliviousOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707890"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="24d40-102">De functie ObliviousOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="24d40-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="24d40-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="24d40-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="24d40-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24d40-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24d40-105">Combineert de Oracle- `DeterministicStateOracle` en `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="24d40-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="24d40-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="24d40-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="24d40-107">ancillaOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="24d40-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="24d40-108">Een status voorbereiding Oracle $A $ van het type dat wordt toegepast `DeterministicStateOracle` op REGI ster $a $.</span><span class="sxs-lookup"><span data-stu-id="24d40-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="24d40-109">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="24d40-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="24d40-110">Een Oracle-$U $ van het type dat `ObliviousOracle` gezamenlijk in het REGI ster $a, s $ wordt ingezet.</span><span class="sxs-lookup"><span data-stu-id="24d40-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="24d40-111">Uitvoer: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="24d40-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="24d40-112">Een Oracle-$O = UA $ van type `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="24d40-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="24d40-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="24d40-113">See Also</span></span>

- [<span data-ttu-id="24d40-114">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="24d40-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="24d40-115">Micro soft. Quantum. Oracles. ObliviousOracle</span><span class="sxs-lookup"><span data-stu-id="24d40-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)