---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: De functie ReflectionOracleFromDeterministicStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: 09de63d615a4d80e2b59deeddc07567aefe7660e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193825"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="1f5c6-102">De functie ReflectionOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="1f5c6-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="1f5c6-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="1f5c6-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="1f5c6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f5c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f5c6-105">Maakt reflectie over een bepaalde status vanuit een Oracle.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="1f5c6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1f5c6-106">Description</span></span>

<span data-ttu-id="1f5c6-107">Op basis van een deterministische status voorbereiding Oracle die wordt vertegenwoordigd door een unitary-matrix $O $, is het resultaat van deze functie een Oracle die een reflectie rond de status $ \ket{\psi} $ die is voor bereid door de Oracle-$O $; dat wil zeggen de status $ \ket{\psi} $, $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="1f5c6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="1f5c6-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="1f5c6-109">Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="1f5c6-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="1f5c6-110">Een Oracle die kopieën van de status $ \ket{\psi} $ voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="1f5c6-111">Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="1f5c6-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="1f5c6-112">Een Oracle die overeenkomt met de status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f5c6-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1f5c6-113">See Also</span></span>

- [<span data-ttu-id="1f5c6-114">Micro soft. Quantum. Oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="1f5c6-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="1f5c6-115">Micro soft. Quantum. Oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="1f5c6-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)