---
uid: Microsoft.Quantum.Canon.CX
title: CX-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: c430525b71ad4ef0812d90a8ff20c41a5d5b8708
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704285"
---
# <a name="cx-operation"></a><span data-ttu-id="f9dc0-102">CX-bewerking</span><span class="sxs-lookup"><span data-stu-id="f9dc0-102">CX operation</span></span>

<span data-ttu-id="f9dc0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f9dc0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f9dc0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f9dc0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f9dc0-105">Past de Controlled-X (CX)-poort toe op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="f9dc0-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="f9dc0-106">$ $ \begin{align} \left (\begin{matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="f9dc0-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f9dc0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f9dc0-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="f9dc0-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f9dc0-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f9dc0-109">Beheer Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="f9dc0-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f9dc0-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f9dc0-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f9dc0-111">Doel-Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="f9dc0-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9dc0-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9dc0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f9dc0-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f9dc0-113">Remarks</span></span>

<span data-ttu-id="f9dc0-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="f9dc0-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="f9dc0-115">en om:</span><span class="sxs-lookup"><span data-stu-id="f9dc0-115">and to:</span></span>

```qsharp
CNOT(control, target);
```