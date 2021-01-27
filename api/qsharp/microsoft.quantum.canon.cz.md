---
uid: Microsoft.Quantum.Canon.CZ
title: Bewerking CZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: cef1544fb76d561cfd0949c84c487550d523bb85
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840709"
---
# <a name="cz-operation"></a><span data-ttu-id="e09d6-102">Bewerking CZ</span><span class="sxs-lookup"><span data-stu-id="e09d6-102">CZ operation</span></span>

<span data-ttu-id="e09d6-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e09d6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e09d6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e09d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e09d6-105">Past de Controlled-Z (CZ)-poort toe aan een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="e09d6-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="e09d6-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="e09d6-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e09d6-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="e09d6-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="e09d6-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e09d6-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e09d6-109">Control Qubit voor de CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="e09d6-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e09d6-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e09d6-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e09d6-111">Doel-Qubit voor de CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="e09d6-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e09d6-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e09d6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e09d6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e09d6-113">Remarks</span></span>

<span data-ttu-id="e09d6-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="e09d6-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```