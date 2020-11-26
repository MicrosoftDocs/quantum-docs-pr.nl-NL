---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 97a55b4bb85095c7d8e8432dfcd1c6d6f7e93cdc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223932"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="16723-102">_prepareEntangledState bewerking</span><span class="sxs-lookup"><span data-stu-id="16723-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="16723-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="16723-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="16723-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="16723-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="16723-105">Op basis van twee registers, wordt de status van de maximally Entangled voor elk paar qubits op de respectieve kassa's voor bereid.</span><span class="sxs-lookup"><span data-stu-id="16723-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="16723-106">Alle qubits moeten beginnen met de ⟩-status | 0.</span><span class="sxs-lookup"><span data-stu-id="16723-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="16723-107">Het resultaat is dat de bijbehorende paren qubits van elk REGI ster zich in de $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $ bevinden.</span><span class="sxs-lookup"><span data-stu-id="16723-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="16723-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="16723-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="16723-109">links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16723-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16723-110">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="16723-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="16723-111">rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16723-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16723-112">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="16723-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="16723-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16723-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

