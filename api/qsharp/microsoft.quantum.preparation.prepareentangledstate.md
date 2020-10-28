---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Bewerking PrepareEntangledState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707867"
---
# <a name="prepareentangledstate-operation"></a><span data-ttu-id="89a87-102">Bewerking PrepareEntangledState</span><span class="sxs-lookup"><span data-stu-id="89a87-102">PrepareEntangledState operation</span></span>

<span data-ttu-id="89a87-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="89a87-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="89a87-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89a87-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89a87-105">Pairwise entangles twee Qubit-registers.</span><span class="sxs-lookup"><span data-stu-id="89a87-105">Pairwise entangles two qubit registers.</span></span>

<span data-ttu-id="89a87-106">Op basis van twee registers wordt de maximally Entangled-status $ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $ tussen elk paar qubits op de respectieve kassa's voor bereid, ervan uitgaande dat elke kassa begint met de status $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="89a87-106">That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.</span></span>

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="89a87-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="89a87-107">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="89a87-108">links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="89a87-108">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="89a87-109">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="89a87-109">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="89a87-110">rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="89a87-110">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="89a87-111">Een Qubit-matrix in de $ \ket{0\cdots 0} $-status</span><span class="sxs-lookup"><span data-stu-id="89a87-111">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="89a87-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89a87-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

