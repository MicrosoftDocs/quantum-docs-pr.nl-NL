---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: De functie DeterministicStateOracleFromStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854560"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="42aa5-102">De functie DeterministicStateOracleFromStateOracle</span><span class="sxs-lookup"><span data-stu-id="42aa5-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="42aa5-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="42aa5-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="42aa5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42aa5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42aa5-105">Converteert een Oracle van het type `StateOracle` naar `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="42aa5-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="42aa5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="42aa5-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="42aa5-107">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42aa5-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42aa5-108">De index voor de vlag Qubit van de `stateOracle` $A $, die expliciet op twee registers reageert: de vlag $f $ en het systeem $s $, bijvoorbeeld $A \ket {0} \_ f\ket {\ psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="42aa5-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="42aa5-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="42aa5-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="42aa5-110">Een status voorbereiding Oracle $A $ van type `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="42aa5-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="42aa5-111">Uitvoer: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="42aa5-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="42aa5-112">Voor de voor bereiding van de Oracle-$A $, maar nu van het type `DeterministicStateOracle` , wordt deze toegepast op een REGI ster waarbij $a, s $ niet langer expliciet gescheiden is, bijvoorbeeld  $A \ket{0\psi} \_ {as} $.</span><span class="sxs-lookup"><span data-stu-id="42aa5-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="42aa5-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="42aa5-113">See Also</span></span>

- [<span data-ttu-id="42aa5-114">Micro soft. Quantum. Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="42aa5-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="42aa5-115">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="42aa5-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)