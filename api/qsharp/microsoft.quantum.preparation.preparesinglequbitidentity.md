---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Bewerking PrepareSingleQubitIdentity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 12a650568aa5682e8fb6498808d188b154527acb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709030"
---
# <a name="preparesinglequbitidentity-operation"></a><span data-ttu-id="e60bb-102">Bewerking PrepareSingleQubitIdentity</span><span class="sxs-lookup"><span data-stu-id="e60bb-102">PrepareSingleQubitIdentity operation</span></span>

<span data-ttu-id="e60bb-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e60bb-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e60bb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e60bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e60bb-105">Bereidt een Qubit voor in de gemengde status maximally.</span><span class="sxs-lookup"><span data-stu-id="e60bb-105">Prepares a qubit in the maximally mixed state.</span></span>

<span data-ttu-id="e60bb-106">De opgegeven Qubit wordt voor bereid in de status $ \boldone/$2 door het depolarizing-kanaal $ $ \begin{align} \Omega (\rho) \mathrel{toe te passen: =} \frac {1} {4} \ sum_ {\mu \in \{ 0, 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $ waarbij $ \sigma \_ i $ de $i $ de Pauli-operator is en waarbij $ \rho $ een dichtheids operator is die een gemengde staat vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="e60bb-106">It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.</span></span>

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e60bb-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="e60bb-107">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="e60bb-108">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e60bb-108">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e60bb-109">Een Qubit waarvan de status moet worden ontpolair op de manier die hierboven wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="e60bb-109">A qubit whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e60bb-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e60bb-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e60bb-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e60bb-111">Remarks</span></span>

<span data-ttu-id="e60bb-112">De gemengde status $ \boldone/$2, waarmee het resultaat van het Toep assen van deze bewerking wordt impliciet beschreven in een status, beschrijft een verwachte waarde voor wille keurige keuzes die zijn gemaakt in deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="e60bb-112">The mixed state $\boldone / 2$ describing the result of applying this operation to a state implicitly describes an expectation value over random choices made in this operation.</span></span>
<span data-ttu-id="e60bb-113">Voor elke afzonderlijke toepassing wordt met deze bewerking echter zuivere statussen aan zuivere staten toegewezen, maar dit gebeurt zoals beschreven in verwachting.</span><span class="sxs-lookup"><span data-stu-id="e60bb-113">Thus, for any single application, this operation maps pure states to pure states, but it acts as described in expectation.</span></span>
<span data-ttu-id="e60bb-114">Met name deze bewerking kan worden gebruikt in process tomography om de *niet-eenheids* onderdelen van een kanaal te meten.</span><span class="sxs-lookup"><span data-stu-id="e60bb-114">In particular, this operation can be used in process tomography to measure the *non-unital* components of a channel.</span></span>