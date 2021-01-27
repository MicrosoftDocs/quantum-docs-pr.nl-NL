---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: De functie ReflectionOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842515"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="4699b-102">De functie ReflectionOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="4699b-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="4699b-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="4699b-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="4699b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4699b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4699b-105">Maakt reflectie over een bepaalde status vanuit een Oracle.</span><span class="sxs-lookup"><span data-stu-id="4699b-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="4699b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4699b-106">Description</span></span>

<span data-ttu-id="4699b-107">Op basis van een deterministische status voorbereiding Oracle die wordt vertegenwoordigd door een unitary-matrix $O $, is het resultaat van deze functie een Oracle die een reflectie rond de status $ \ket{\psi} $ die is voor bereid door de Oracle-$O $; dat wil zeggen de status $ \ket{\psi} $, $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="4699b-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="4699b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4699b-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="4699b-109">Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="4699b-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="4699b-110">Een Oracle die kopieën van de status $ \ket{\psi} $ voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="4699b-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="4699b-111">Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="4699b-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="4699b-112">Een Oracle die overeenkomt met de status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="4699b-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="4699b-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4699b-113">See Also</span></span>

- [<span data-ttu-id="4699b-114">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="4699b-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="4699b-115">Micro soft. Quantum. Oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="4699b-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)