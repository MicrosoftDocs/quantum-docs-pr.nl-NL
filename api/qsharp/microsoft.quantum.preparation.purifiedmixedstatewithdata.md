---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: De functie PurifiedMixedStateWithData
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: fc7bf8e6157af079ae4233ef45e67ce8ddfb8fe3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854283"
---
# <a name="purifiedmixedstatewithdata-function"></a><span data-ttu-id="31641-102">De functie PurifiedMixedStateWithData</span><span class="sxs-lookup"><span data-stu-id="31641-102">PurifiedMixedStateWithData function</span></span>

<span data-ttu-id="31641-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="31641-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="31641-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31641-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31641-105">Retourneert een bewerking die een zuivering van een bepaalde gemengde status voorbereidt, Entangled met een REGI ster dat een bepaalde verzameling gegevens vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="31641-105">Returns an operation that prepares a a purification of a given mixed state, entangled with a register representing a given collection of data.</span></span>
<span data-ttu-id="31641-106">Een ' zuivere gemengde status met gegevens ' verwijst naar een status van de vorm σi √ Pi | i ⟩ | XI ⟩ | garbagei ⟩, waarbij elke XI een bitstring is voor het coderen van extra gegevens die zijn gekoppeld aan de kassa | i ⟩.</span><span class="sxs-lookup"><span data-stu-id="31641-106">A "purified mixed state with data" refers to a state of the form Σᵢ √𝑝ᵢ |𝑖⟩ |𝑥ᵢ⟩ |garbageᵢ⟩, where each 𝑥ᵢ is a bitstring encoding additional data associated with the register |𝑖⟩.</span></span>

<span data-ttu-id="31641-107">Zie https://arxiv.org/pdf/1805.03662.pdf?page=15 voor meer discussie.</span><span class="sxs-lookup"><span data-stu-id="31641-107">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="31641-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="31641-108">Description</span></span>

<span data-ttu-id="31641-109">Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven. deze representatie wordt geretourneerd als een status voorbereidings bewerking.</span><span class="sxs-lookup"><span data-stu-id="31641-109">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="31641-110">Met name een lijst van $N $ coëfficiënten $ \ alpha_j $ en een bitstring $ \vec{x}_j $ die is gekoppeld aan elke coëfficiënt, deze functie retourneert een bewerking die gebruikmaakt van de Quantum rom-techniek om een benadering voor te bereiden $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {N-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x}_j} \end{align} $ $ van de gemengde status $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ FRAC {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{align} $ $ waarbij elke $p _j $ een benadering is van de gegeven coëfficiënt $ \ alpha_j $, zoals $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ voor elke $j $.</span><span class="sxs-lookup"><span data-stu-id="31641-110">In particular, given a list of $N$ coefficients $\alpha_j$, and a bitstring $\vec{x}_j$ associated with each coefficient, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="31641-111">Bij het door gegeven van een index register en een REGI ster van garbage qubits, in eerste instantie in de status $ \ket {0} \ket{00\cdots 0}, met de geretourneerde bewerking worden beide registers voor bereid op de zuivering van $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _J} \ket{\text{garbage} _J}, \end{align} $ $, waardoor het opnieuw instellen en ongedaan maken van de garbagecollection de gewenste voor bereiding krijgt in de doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="31641-111">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j} \ket{\vec{x}_j} \ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="31641-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="31641-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="31641-113">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="31641-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="31641-114">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="31641-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--doublebool"></a><span data-ttu-id="31641-115">coëfficiënten: ([dubbel](xref:microsoft.quantum.lang-ref.double),[BOOL](xref:microsoft.quantum.lang-ref.bool)[]) []</span><span class="sxs-lookup"><span data-stu-id="31641-115">coefficients : ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[])[]</span></span>

<span data-ttu-id="31641-116">Matrix van $N $ coëfficiënten waarmee de kans van basis status wordt opgegeven, samen met de bitstring $ \vec{x} _j $ die aan elke coëfficiënt is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="31641-116">Array of $N$ coefficients specifying the probability of basis states, along with the bitstring $\vec{x}_j$ associated with each coefficient.</span></span>
<span data-ttu-id="31641-117">Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="31641-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="31641-118">Uitvoer: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="31641-118">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="31641-119">Een bewerking waarbij $ \tilde \rho $ als zuivering wordt voor bereid op een gemeen schappelijke index en een schone registratie.</span><span class="sxs-lookup"><span data-stu-id="31641-119">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="31641-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="31641-120">Remarks</span></span>

<span data-ttu-id="31641-121">De coëfficiënten die aan deze bewerking worden gegeven, worden genormaliseerd volgens de 1-norm, zodat de coëfficiënten altijd worden beschouwd als een geldige categorische-kans-distributie.</span><span class="sxs-lookup"><span data-stu-id="31641-121">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="31641-122">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="31641-122">References</span></span>

- <span data-ttu-id="31641-123">Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="31641-123">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="31641-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="31641-124">See Also</span></span>

- [<span data-ttu-id="31641-125">Micro soft. Quantum. prepare. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="31641-125">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)