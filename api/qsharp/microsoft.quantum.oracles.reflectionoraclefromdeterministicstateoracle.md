---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: De functie ReflectionOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c2d37216aebcdc5243d0f1d6ec9db261cc9bd0c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707872"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="447f0-102">De functie ReflectionOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="447f0-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="447f0-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="447f0-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="447f0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="447f0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="447f0-105">Maakt reflectie over een bepaalde status vanuit een Oracle.</span><span class="sxs-lookup"><span data-stu-id="447f0-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="447f0-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="447f0-106">Description</span></span>

<span data-ttu-id="447f0-107">Op basis van een deterministische status voorbereiding Oracle die wordt vertegenwoordigd door een unitary-matrix $O $, is het resultaat van deze functie een Oracle die een reflectie rond de status $ \ket{\psi} $ die is voor bereid door de Oracle-$O $; dat wil zeggen de status $ \ket{\psi} $, $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="447f0-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="447f0-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="447f0-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="447f0-109">Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="447f0-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="447f0-110">Een Oracle die kopieën van de status $ \ket{\psi} $ voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="447f0-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="447f0-111">Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="447f0-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="447f0-112">Een Oracle die overeenkomt met de status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="447f0-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="447f0-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="447f0-113">See Also</span></span>

- [<span data-ttu-id="447f0-114">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="447f0-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="447f0-115">Micro soft. Quantum. Oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="447f0-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)