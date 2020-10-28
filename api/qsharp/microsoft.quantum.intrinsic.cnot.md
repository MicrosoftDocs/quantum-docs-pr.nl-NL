---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Bewerking CNOT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 2fb5b4df189fb3ab23b2ca5cb273b2451ffcc067
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708082"
---
# <a name="cnot-operation"></a><span data-ttu-id="d61e6-102">Bewerking CNOT</span><span class="sxs-lookup"><span data-stu-id="d61e6-102">CNOT operation</span></span>

<span data-ttu-id="d61e6-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d61e6-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d61e6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d61e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d61e6-105">Past de Controlled-NOT (CNOT)-poort toe op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="d61e6-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="d61e6-106">\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="d61e6-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="d61e6-107">waar rijen en kolommen worden besteld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="d61e6-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d61e6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d61e6-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="d61e6-109">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d61e6-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d61e6-110">Control Qubit voor de CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="d61e6-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d61e6-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d61e6-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d61e6-112">Doel-Qubit voor de CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="d61e6-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d61e6-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d61e6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d61e6-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d61e6-114">Remarks</span></span>

<span data-ttu-id="d61e6-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="d61e6-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```