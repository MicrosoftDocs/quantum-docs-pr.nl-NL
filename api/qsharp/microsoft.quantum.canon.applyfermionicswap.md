---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Bewerking ApplyFermionicSWAP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 334f407a32dabc8f4e0a1a29c8f06a1b9f40dc59
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845058"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="02286-102">Bewerking ApplyFermionicSWAP</span><span class="sxs-lookup"><span data-stu-id="02286-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="02286-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="02286-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="02286-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02286-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02286-105">Hiermee past u de Fermionic-SWAP toe.</span><span class="sxs-lookup"><span data-stu-id="02286-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="02286-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02286-106">Description</span></span>

<span data-ttu-id="02286-107">Hiermee wordt de qubits vervangen tijdens het Toep assen van een globale fase van-1 als beide qubits 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="02286-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="02286-108">Hiermee behoudt u anti-symmetrization van banen.</span><span class="sxs-lookup"><span data-stu-id="02286-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="02286-109">Zie  voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="02286-109">See  for more information.</span></span>

<span data-ttu-id="02286-110">Deze bewerking wordt vertegenwoordigd door de unitary-operator \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="02286-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="02286-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="02286-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="02286-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="02286-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="02286-113">qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="02286-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="02286-114">De eerste Qubit die moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="02286-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="02286-115">qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="02286-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="02286-116">Het tweede Qubit dat moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="02286-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="02286-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02286-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="02286-118">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="02286-118">References</span></span>

- [<span data-ttu-id="02286-119">*Ryan Babbush, Nathan Wiebe, Jarrod McClean, Jeroen McClain, Hartmut neven, Garnet Kin-Lic kanaal*, arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="02286-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="02286-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="02286-120">See Also</span></span>

- [<span data-ttu-id="02286-121">Micro soft. Quantum. intrinsiek. SWAP</span><span class="sxs-lookup"><span data-stu-id="02286-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)