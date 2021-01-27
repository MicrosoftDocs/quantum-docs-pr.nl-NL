---
uid: Microsoft.Quantum.Canon.CX
title: CX-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: e27b30a6b4609daaac2cc5eda68120115777af0c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840759"
---
# <a name="cx-operation"></a><span data-ttu-id="02753-102">CX-bewerking</span><span class="sxs-lookup"><span data-stu-id="02753-102">CX operation</span></span>

<span data-ttu-id="02753-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="02753-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="02753-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02753-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02753-105">Past de Controlled-X (CX)-poort toe op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="02753-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="02753-106">$ $ \begin{align} \left (\begin{matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="02753-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="02753-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="02753-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="02753-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="02753-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="02753-109">Beheer Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="02753-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="02753-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="02753-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="02753-111">Doel-Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="02753-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="02753-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02753-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="02753-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="02753-113">Remarks</span></span>

<span data-ttu-id="02753-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="02753-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="02753-115">en om:</span><span class="sxs-lookup"><span data-stu-id="02753-115">and to:</span></span>

```qsharp
CNOT(control, target);
```