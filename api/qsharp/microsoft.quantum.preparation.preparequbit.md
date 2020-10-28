---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Bewerking PrepareQubit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 5f42bf26a8f9638ea88c035a18846050c3776b45
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708226"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="2afa1-102">Bewerking PrepareQubit</span><span class="sxs-lookup"><span data-stu-id="2afa1-102">PrepareQubit operation</span></span>

<span data-ttu-id="2afa1-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2afa1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2afa1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2afa1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2afa1-105">Bereidt een Qubit voor in de + 1 ( `Zero` ) eigenstate van de gegeven Pauli-operator.</span><span class="sxs-lookup"><span data-stu-id="2afa1-105">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="2afa1-106">Als de identiteits operator wordt opgegeven, wordt de Qubit voor bereid in de gemengde status maximally.</span><span class="sxs-lookup"><span data-stu-id="2afa1-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="2afa1-107">Als de Qubit in eerste instantie de $ \ket {0} $-status had, bereidt deze bewerking de Qubit voor in de $ + $1-eigenstate van een bepaalde Pauli-operator of, `PauliI` in plaats daarvan, in de gemengde status maximally (Zie <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="2afa1-107">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="2afa1-108">Als de Qubit een andere status heeft dan $ \ket {0} $, geldt deze bewerking voor de volgende poorten: $H $ voor `PauliX` , $HS $ voor `PauliY` , $I $ voor `PauliZ` en <xref:microsoft.quantum.preparation.preparesinglequbitidentity> voor `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="2afa1-108">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2afa1-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="2afa1-109">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="2afa1-110">basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="2afa1-110">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="2afa1-111">Een Pauli-operator $P $.</span><span class="sxs-lookup"><span data-stu-id="2afa1-111">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2afa1-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2afa1-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2afa1-113">Een Qubit die moet worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="2afa1-113">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2afa1-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2afa1-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

