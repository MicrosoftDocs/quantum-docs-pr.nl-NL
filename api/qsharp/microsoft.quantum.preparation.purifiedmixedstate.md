---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: De functie PurifiedMixedState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 73b031f1082d0a12975abad074b07184dcbabdbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230018"
---
# <a name="purifiedmixedstate-function"></a><span data-ttu-id="b1143-102">De functie PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="b1143-102">PurifiedMixedState function</span></span>

<span data-ttu-id="b1143-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b1143-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b1143-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b1143-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b1143-105">Retourneert een bewerking die een zuivering van een bepaalde gemengde status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="b1143-105">Returns an operation that prepares a a purification of a given mixed state.</span></span>
<span data-ttu-id="b1143-106">Een ' zuivere gemengde status ' verwijst naar de statussen van het formulier | ψ ⟩ = σi √ Pi | i ⟩ | garbagei ⟩, opgegeven door een vector van coëfficiënten {pi}.</span><span class="sxs-lookup"><span data-stu-id="b1143-106">A "purified mixed state" refers to states of the form |ψ⟩ = Σᵢ √𝑝ᵢ |𝑖⟩ |garbageᵢ⟩ specified by a vector of coefficients {𝑝ᵢ}.</span></span> <span data-ttu-id="b1143-107">De statussen van dit formulier kunnen worden verkleind tot gemengde statussen ρ ≔ Pi | i ⟩ ⟨ i | door over te trekken van de registratie van ' garbage ' (dat wil zeggen, een gemengde status die diagonaal is in de berekening).</span><span class="sxs-lookup"><span data-stu-id="b1143-107">States of this form can be reduced to mixed states ρ ≔ 𝑝ᵢ |𝑖⟩⟨𝑖| by tracing over the "garbage" register (that is, a mixed state that is diagonal in the computational basis).</span></span>

<span data-ttu-id="b1143-108">Zie https://arxiv.org/pdf/1805.03662.pdf?page=15 voor meer discussie.</span><span class="sxs-lookup"><span data-stu-id="b1143-108">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="b1143-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b1143-109">Description</span></span>

<span data-ttu-id="b1143-110">Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven. deze representatie wordt geretourneerd als een status voorbereidings bewerking.</span><span class="sxs-lookup"><span data-stu-id="b1143-110">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="b1143-111">Met name een lijst van $N $-coëfficiënten $ \ alpha_j $, deze functie retourneert een bewerking die gebruikmaakt van de Quantum ROM-techniek om een benadering voor te bereiden $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \end{align} $ $ van de gemengde status $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ FRAC {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{align} $ $ waarbij elke $p _j $ een benadering is van de gegeven coëfficiënt $ \ alpha_j $, \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ voor elke $j $.</span><span class="sxs-lookup"><span data-stu-id="b1143-111">In particular, given a list of $N$ coefficients $\alpha_j$, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="b1143-112">Bij het door gegeven van een index register en een REGI ster van garbage qubits, in eerste instantie van de status $ \ket {0} \ket{00\cdots 0} bereidt de geretourneerde bewerking beide registers voor op de zuivering van $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _J}, \end{align} $ $, waardoor het opnieuw instellen en ongedaan maken van de garbage collector de gewenste voor bereiding krijgt in de doel fout</span><span class="sxs-lookup"><span data-stu-id="b1143-112">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="b1143-113">Invoer</span><span class="sxs-lookup"><span data-stu-id="b1143-113">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="b1143-114">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b1143-114">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b1143-115">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="b1143-115">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="b1143-116">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b1143-116">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b1143-117">Matrix van $N $-coëfficiënten waarmee de kans op basis status wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="b1143-117">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="b1143-118">Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="b1143-118">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="b1143-119">Uitvoer: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="b1143-119">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="b1143-120">Een bewerking waarbij $ \tilde \rho $ als zuivering wordt voor bereid op een gemeen schappelijke index en een schone registratie.</span><span class="sxs-lookup"><span data-stu-id="b1143-120">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1143-121">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b1143-121">Remarks</span></span>

<span data-ttu-id="b1143-122">De coëfficiënten die aan deze bewerking worden gegeven, worden genormaliseerd volgens de 1-norm, zodat de coëfficiënten altijd worden beschouwd als een geldige categorische-kans-distributie.</span><span class="sxs-lookup"><span data-stu-id="b1143-122">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="b1143-123">Referenties</span><span class="sxs-lookup"><span data-stu-id="b1143-123">References</span></span>

- <span data-ttu-id="b1143-124">Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="b1143-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="b1143-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b1143-125">See Also</span></span>

- [<span data-ttu-id="b1143-126">Micro soft. Quantum. prepare. PurifiedMixedStateWithData</span><span class="sxs-lookup"><span data-stu-id="b1143-126">Microsoft.Quantum.Preparation.PurifiedMixedStateWithData</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)