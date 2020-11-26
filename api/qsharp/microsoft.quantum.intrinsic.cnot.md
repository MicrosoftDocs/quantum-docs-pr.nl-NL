---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Bewerking CNOT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 90e84f7d0ea7373498632474dfafa23335f0c78e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198973"
---
# <a name="cnot-operation"></a><span data-ttu-id="c89d1-102">Bewerking CNOT</span><span class="sxs-lookup"><span data-stu-id="c89d1-102">CNOT operation</span></span>

<span data-ttu-id="c89d1-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c89d1-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c89d1-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c89d1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c89d1-105">Past de Controlled-NOT (CNOT)-poort toe op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="c89d1-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="c89d1-106">\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="c89d1-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="c89d1-107">waar rijen en kolommen worden besteld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="c89d1-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c89d1-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c89d1-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="c89d1-109">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c89d1-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c89d1-110">Control Qubit voor de CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="c89d1-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c89d1-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c89d1-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c89d1-112">Doel-Qubit voor de CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="c89d1-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c89d1-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c89d1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c89d1-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c89d1-114">Remarks</span></span>

<span data-ttu-id="c89d1-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="c89d1-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```