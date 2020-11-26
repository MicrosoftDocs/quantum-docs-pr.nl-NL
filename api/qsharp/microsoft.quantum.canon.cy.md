---
uid: Microsoft.Quantum.Canon.CY
title: CY-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4a1a533421dd9205e973d5e8237d67b20bc4886d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216571"
---
# <a name="cy-operation"></a><span data-ttu-id="bdde4-102">CY-bewerking</span><span class="sxs-lookup"><span data-stu-id="bdde4-102">CY operation</span></span>

<span data-ttu-id="bdde4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bdde4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bdde4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bdde4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bdde4-105">Hiermee wordt de beheerde Y-poort (CY) toegepast op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="bdde4-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="bdde4-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & ik & 0 \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum concepten Guide.</span><span class="sxs-lookup"><span data-stu-id="bdde4-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bdde4-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="bdde4-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="bdde4-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bdde4-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bdde4-109">Beheer Qubit voor de CY-poort.</span><span class="sxs-lookup"><span data-stu-id="bdde4-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bdde4-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bdde4-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bdde4-111">Doel-Qubit voor de CY-Gate.</span><span class="sxs-lookup"><span data-stu-id="bdde4-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bdde4-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bdde4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bdde4-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="bdde4-113">Remarks</span></span>

<span data-ttu-id="bdde4-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="bdde4-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```