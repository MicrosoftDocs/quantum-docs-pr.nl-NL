---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Bewerking PrepareEntangledState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 5f6e3ea1e7638d3bc446f21ace2968cf8284353a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210468"
---
# <a name="prepareentangledstate-operation"></a><span data-ttu-id="ba2ed-102">Bewerking PrepareEntangledState</span><span class="sxs-lookup"><span data-stu-id="ba2ed-102">PrepareEntangledState operation</span></span>

<span data-ttu-id="ba2ed-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="ba2ed-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="ba2ed-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba2ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba2ed-105">Pairwise entangles twee Qubit-registers.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-105">Pairwise entangles two qubit registers.</span></span>

<span data-ttu-id="ba2ed-106">Op basis van twee registers wordt de maximally Entangled-status $ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $ tussen elk paar qubits op de respectieve kassa's voor bereid, ervan uitgaande dat elke kassa begint met de status $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-106">That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.</span></span>

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ba2ed-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="ba2ed-107">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="ba2ed-108">links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ba2ed-108">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ba2ed-109">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="ba2ed-109">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="ba2ed-110">rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ba2ed-110">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ba2ed-111">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="ba2ed-111">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="ba2ed-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ba2ed-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

