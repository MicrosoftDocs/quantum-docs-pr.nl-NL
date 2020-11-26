---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Bewerking PreparePauliEigenstate
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: b24852bb3a455a9fe04b3535156d0c3dfb1a7d12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193689"
---
# <a name="preparepaulieigenstate-operation"></a><span data-ttu-id="3be2f-102">Bewerking PreparePauliEigenstate</span><span class="sxs-lookup"><span data-stu-id="3be2f-102">PreparePauliEigenstate operation</span></span>

<span data-ttu-id="3be2f-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="3be2f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="3be2f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3be2f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3be2f-105">Bereidt een Qubit voor in de positieve eigenstate van een bepaalde Pauli-operator.</span><span class="sxs-lookup"><span data-stu-id="3be2f-105">Prepares a qubit in the positive eigenstate of a given Pauli operator.</span></span>
<span data-ttu-id="3be2f-106">Als de identiteits operator wordt opgegeven, wordt de Qubit voor bereid in de gemengde status maximally.</span><span class="sxs-lookup"><span data-stu-id="3be2f-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="3be2f-107">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3be2f-107">Description</span></span>

<span data-ttu-id="3be2f-108">Als de Qubit in eerste instantie de $ \ket {0} $-status had, bereidt deze bewerking de Qubit voor in de $ + $1-eigenstate van een bepaalde Pauli-operator of, `PauliI` in plaats daarvan, in de gemengde status maximally (Zie <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="3be2f-108">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="3be2f-109">Als de Qubit een andere status heeft dan $ \ket {0} $, geldt deze bewerking voor de volgende poorten: $H $ voor `PauliX` , $HS $ voor `PauliY` , $I $ voor `PauliZ` en <xref:microsoft.quantum.preparation.preparesinglequbitidentity> voor `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="3be2f-109">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

## <a name="input"></a><span data-ttu-id="3be2f-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="3be2f-110">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="3be2f-111">basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="3be2f-111">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="3be2f-112">Een Pauli-operator $P $.</span><span class="sxs-lookup"><span data-stu-id="3be2f-112">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="3be2f-113">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3be2f-113">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3be2f-114">Een Qubit die moet worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="3be2f-114">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3be2f-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3be2f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

