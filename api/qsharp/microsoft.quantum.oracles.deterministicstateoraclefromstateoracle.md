---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: De functie DeterministicStateOracleFromStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226754"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="39c4d-102">De functie DeterministicStateOracleFromStateOracle</span><span class="sxs-lookup"><span data-stu-id="39c4d-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="39c4d-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="39c4d-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="39c4d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39c4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39c4d-105">Converteert een Oracle van het type `StateOracle` naar `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="39c4d-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="39c4d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="39c4d-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="39c4d-107">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39c4d-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39c4d-108">De index voor de vlag Qubit van de `stateOracle` $A $, die expliciet op twee registers reageert: de vlag $f $ en het systeem $s $, bijvoorbeeld $A \ket {0} \_ f\ket {\ psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="39c4d-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="39c4d-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="39c4d-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="39c4d-110">Een status voorbereiding Oracle $A $ van type `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="39c4d-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="39c4d-111">Uitvoer: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="39c4d-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="39c4d-112">Voor de voor bereiding van de Oracle-$A $, maar nu van het type `DeterministicStateOracle` , wordt deze toegepast op een REGI ster waarbij $a, s $ niet langer expliciet gescheiden is, bijvoorbeeld  $A \ket{0\psi} \_ {as} $.</span><span class="sxs-lookup"><span data-stu-id="39c4d-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="39c4d-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="39c4d-113">See Also</span></span>

- [<span data-ttu-id="39c4d-114">Micro soft. Quantum. Oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="39c4d-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="39c4d-115">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="39c4d-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)