---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: Wissel bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 18b910741e9d0883fc5fcd025eb647407c823269
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706525"
---
# <a name="swap-operation"></a><span data-ttu-id="68ed8-102">Wissel bewerking</span><span class="sxs-lookup"><span data-stu-id="68ed8-102">SWAP operation</span></span>

<span data-ttu-id="68ed8-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="68ed8-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="68ed8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="68ed8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="68ed8-105">Hiermee wordt de SWAP-Gate toegepast op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="68ed8-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="68ed8-106">\begin{align} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="68ed8-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="68ed8-107">waar rijen en kolommen worden besteld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="68ed8-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="68ed8-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="68ed8-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="68ed8-109">qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="68ed8-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="68ed8-110">De eerste Qubit die moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="68ed8-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="68ed8-111">qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="68ed8-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="68ed8-112">Het tweede Qubit dat moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="68ed8-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="68ed8-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="68ed8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="68ed8-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="68ed8-114">Remarks</span></span>

<span data-ttu-id="68ed8-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="68ed8-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```