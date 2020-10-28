---
uid: Microsoft.Quantum.Canon.CZ
title: Bewerking CZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: bc38cd43a0dcaf7aea735ef6468a394e91c85593
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704269"
---
# <a name="cz-operation"></a><span data-ttu-id="8f661-102">Bewerking CZ</span><span class="sxs-lookup"><span data-stu-id="8f661-102">CZ operation</span></span>

<span data-ttu-id="8f661-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f661-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f661-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8f661-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8f661-105">Past de Controlled-Z (CZ)-poort toe aan een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="8f661-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="8f661-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="8f661-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="8f661-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="8f661-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="8f661-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f661-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f661-109">Control Qubit voor de CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="8f661-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8f661-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f661-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f661-111">Doel-Qubit voor de CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="8f661-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f661-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f661-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8f661-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8f661-113">Remarks</span></span>

<span data-ttu-id="8f661-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="8f661-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```