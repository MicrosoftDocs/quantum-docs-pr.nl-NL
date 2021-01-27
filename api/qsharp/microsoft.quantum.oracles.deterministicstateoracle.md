---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Door de gebruiker gedefinieerd DeterministicStateOracle-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842595"
---
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="ed324-102">Door de gebruiker gedefinieerd DeterministicStateOracle-type</span><span class="sxs-lookup"><span data-stu-id="ed324-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="ed324-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="ed324-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="ed324-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed324-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed324-105">Vertegenwoordigt een Oracle voor deterministische status voorbereiding.</span><span class="sxs-lookup"><span data-stu-id="ed324-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="ed324-106">De invoer voor de Oracle-$O $ is:</span><span class="sxs-lookup"><span data-stu-id="ed324-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="ed324-107">Het REGI ster waarin de gewenste Quantum status $ \ket{\psi} \_ s $ wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ed324-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="ed324-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ed324-108">Remarks</span></span>

<span data-ttu-id="ed324-109">Deze Oracle die is gedefinieerd door $O \ket {0} = \ket{\psi} $, treedt op in de status op basis van de berekening $ \ket {0} $ om de status $ \ket{\psi} $ te maken.</span><span class="sxs-lookup"><span data-stu-id="ed324-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="ed324-110">De eerste para meter is het Qubit-REGI ster van $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="ed324-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>