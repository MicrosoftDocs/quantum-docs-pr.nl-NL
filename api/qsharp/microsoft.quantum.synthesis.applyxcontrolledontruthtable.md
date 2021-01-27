---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Bewerking ApplyXControlledOnTruthTable
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 6e956038f7cd15db7348ff830da8bc9eae53aa61
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855566"
---
# <a name="applyxcontrolledontruthtable-operation"></a><span data-ttu-id="96dc3-102">Bewerking ApplyXControlledOnTruthTable</span><span class="sxs-lookup"><span data-stu-id="96dc3-102">ApplyXControlledOnTruthTable operation</span></span>

<span data-ttu-id="96dc3-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="96dc3-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="96dc3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="96dc3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="96dc3-105">De bewerking wordt toegepast @"microsoft.quantum.intrinsic.x" op `target` als de Boole-functie `func` resulteert in waar voor de klassieke toewijzing in `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="96dc3-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="96dc3-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="96dc3-106">Description</span></span>

<span data-ttu-id="96dc3-107">Met deze bewerking wordt de unitary-bewerking geïmplementeerd \begin{align} U\ket {x} \ Ket {y} = \ket{x}\ket{y \oplus f (x)} \end{align} waarbij respectievelijk $x $ en $y $ representeren `controlRegister` `target` .</span><span class="sxs-lookup"><span data-stu-id="96dc3-107">The operation implements the unitary operation \begin{align} U\ket{x}\ket{y} = \ket{x}\ket{y \oplus f(x)} \end{align} where $x$ and $y$ represent `controlRegister` and `target`, respectively.</span></span>

<span data-ttu-id="96dc3-108">De Booleaanse functie $f $ wordt weer gegeven als een waarheids tabel in termen van een groot geheel getal.</span><span class="sxs-lookup"><span data-stu-id="96dc3-108">The Boolean function $f$ is represented as a truth table in terms of a big integer.</span></span>
<span data-ttu-id="96dc3-109">De functie meerderheid op drie invoer wordt bijvoorbeeld vertegenwoordigd door de bitstring `11101000` , waarbij de meest significante bit `1` overeenkomt met de invoer toewijzing `(1, 1, 1)` en de minst significante bit `0` overeenkomt met de invoer toewijzing `(0, 0, 0)` .</span><span class="sxs-lookup"><span data-stu-id="96dc3-109">For example, the majority function on three inputs is represented by the bitstring `11101000`, where the most significant bit `1` corresponds to the input assignment `(1, 1, 1)`, and the least significant bit `0` corresponds to the input assignment `(0, 0, 0)`.</span></span>
<span data-ttu-id="96dc3-110">De waarde kan worden weer gegeven met het grote gehele getal `0xE8L` in hexadecimale notatie of als `232L` in de decimale notatie.</span><span class="sxs-lookup"><span data-stu-id="96dc3-110">It can be represented by the big integer `0xE8L` in hexadecimal notation or as `232L` in decimal notation.</span></span>  <span data-ttu-id="96dc3-111">Het `L` achtervoegsel geeft aan dat de constante van het type is `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="96dc3-111">The `L` suffix indicates that the constant is of type `BigInt`.</span></span>
<span data-ttu-id="96dc3-112">Meer informatie over deze representatie vindt u ook in de [waarheids tabellen Kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span><span class="sxs-lookup"><span data-stu-id="96dc3-112">More details on this representation can also be found in the [truth tables kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span></span>

<span data-ttu-id="96dc3-113">De implementatie maakt gebruik van @"microsoft.quantum.intrinsic.cnot" en @"microsoft.quantum.intrinsic.r1" poorten.</span><span class="sxs-lookup"><span data-stu-id="96dc3-113">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>

## <a name="input"></a><span data-ttu-id="96dc3-114">Invoer</span><span class="sxs-lookup"><span data-stu-id="96dc3-114">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="96dc3-115">FUNC: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="96dc3-115">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="96dc3-116">Tabel met Boole-waarheid wordt weer gegeven als Big-geheel getal</span><span class="sxs-lookup"><span data-stu-id="96dc3-116">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="96dc3-117">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="96dc3-117">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="96dc3-118">REGI ster van controle qubits</span><span class="sxs-lookup"><span data-stu-id="96dc3-118">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="96dc3-119">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="96dc3-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="96dc3-120">Doel-Qubit</span><span class="sxs-lookup"><span data-stu-id="96dc3-120">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="96dc3-121">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="96dc3-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="96dc3-122">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="96dc3-122">References</span></span>

- [<span data-ttu-id="96dc3-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv: Quant-pH/0303063</span><span class="sxs-lookup"><span data-stu-id="96dc3-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv:quant-ph/0303063</span></span>](https://arxiv.org/abs/quant-ph/0303063)
- [<span data-ttu-id="96dc3-124">*Mathias soeken*, *Martin Roetteler*, arXiv: 2005.12310</span><span class="sxs-lookup"><span data-stu-id="96dc3-124">*Mathias Soeken*, *Martin Roetteler*, arXiv:2005.12310</span></span>](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a><span data-ttu-id="96dc3-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="96dc3-125">See Also</span></span>

- [<span data-ttu-id="96dc3-126">Micro soft. Quantum. synthese. ApplyXControlledOnTruthTableWithCleanTarget</span><span class="sxs-lookup"><span data-stu-id="96dc3-126">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)