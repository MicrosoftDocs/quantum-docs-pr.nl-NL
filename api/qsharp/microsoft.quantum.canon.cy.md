---
uid: Microsoft.Quantum.Canon.CY
title: CY-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 291891457ff39cf7092d17aa1d900dd0d35d9cf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704277"
---
# <a name="cy-operation"></a><span data-ttu-id="acdb1-102">CY-bewerking</span><span class="sxs-lookup"><span data-stu-id="acdb1-102">CY operation</span></span>

<span data-ttu-id="acdb1-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="acdb1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="acdb1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="acdb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="acdb1-105">Hiermee wordt de beheerde Y-poort (CY) toegepast op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="acdb1-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="acdb1-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & ik & 0 \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum concepten Guide.</span><span class="sxs-lookup"><span data-stu-id="acdb1-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="acdb1-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="acdb1-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="acdb1-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="acdb1-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="acdb1-109">Beheer Qubit voor de CY-poort.</span><span class="sxs-lookup"><span data-stu-id="acdb1-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="acdb1-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="acdb1-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="acdb1-111">Doel-Qubit voor de CY-Gate.</span><span class="sxs-lookup"><span data-stu-id="acdb1-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="acdb1-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="acdb1-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="acdb1-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="acdb1-113">Remarks</span></span>

<span data-ttu-id="acdb1-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="acdb1-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```