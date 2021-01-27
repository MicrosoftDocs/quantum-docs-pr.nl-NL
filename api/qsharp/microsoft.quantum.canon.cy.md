---
uid: Microsoft.Quantum.Canon.CY
title: CY-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 862f058e630ee6d9159e0fe514ca2dd1179ea9a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840739"
---
# <a name="cy-operation"></a><span data-ttu-id="6426a-102">CY-bewerking</span><span class="sxs-lookup"><span data-stu-id="6426a-102">CY operation</span></span>

<span data-ttu-id="6426a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6426a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6426a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6426a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6426a-105">Hiermee wordt de beheerde Y-poort (CY) toegepast op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="6426a-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="6426a-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & ik & 0 \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum concepten Guide.</span><span class="sxs-lookup"><span data-stu-id="6426a-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6426a-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="6426a-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="6426a-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6426a-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6426a-109">Beheer Qubit voor de CY-poort.</span><span class="sxs-lookup"><span data-stu-id="6426a-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6426a-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6426a-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6426a-111">Doel-Qubit voor de CY-Gate.</span><span class="sxs-lookup"><span data-stu-id="6426a-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6426a-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6426a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6426a-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6426a-113">Remarks</span></span>

<span data-ttu-id="6426a-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="6426a-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```