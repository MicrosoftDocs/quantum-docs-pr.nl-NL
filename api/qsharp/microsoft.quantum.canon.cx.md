---
uid: Microsoft.Quantum.Canon.CX
title: CX-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4eaecf372f3054de4886b1e42c6b4ce386a22f73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207238"
---
# <a name="cx-operation"></a><span data-ttu-id="f37ba-102">CX-bewerking</span><span class="sxs-lookup"><span data-stu-id="f37ba-102">CX operation</span></span>

<span data-ttu-id="f37ba-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f37ba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f37ba-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f37ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f37ba-105">Past de Controlled-X (CX)-poort toe op een paar qubits.</span><span class="sxs-lookup"><span data-stu-id="f37ba-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="f37ba-106">$ $ \begin{align} \left (\begin{matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $ $ waar rijen en kolommen zijn ingedeeld als in de Quantum begrippen-hand leiding.</span><span class="sxs-lookup"><span data-stu-id="f37ba-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f37ba-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f37ba-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="f37ba-108">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f37ba-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f37ba-109">Beheer Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="f37ba-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f37ba-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f37ba-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f37ba-111">Doel-Qubit voor de CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="f37ba-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f37ba-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f37ba-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f37ba-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f37ba-113">Remarks</span></span>

<span data-ttu-id="f37ba-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="f37ba-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="f37ba-115">en om:</span><span class="sxs-lookup"><span data-stu-id="f37ba-115">and to:</span></span>

```qsharp
CNOT(control, target);
```