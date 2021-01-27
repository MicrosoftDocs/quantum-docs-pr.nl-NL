---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Bewerking ApplyOpRepeatedlyOverC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 1cf3f32f0d25c1b4437f2bdbd93171a1a2e1e760
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844783"
---
# <a name="applyoprepeatedlyoverc-operation"></a><span data-ttu-id="b4569-102">Bewerking ApplyOpRepeatedlyOverC</span><span class="sxs-lookup"><span data-stu-id="b4569-102">ApplyOpRepeatedlyOverC operation</span></span>

<span data-ttu-id="b4569-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b4569-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b4569-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4569-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4569-105">Past hetzelfde op een Qubit-REGI ster meerdere keren toe.</span><span class="sxs-lookup"><span data-stu-id="b4569-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="b4569-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b4569-106">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="b4569-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="b4569-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b4569-108">Een bewerking die meerdere keren wordt toegepast op het Qubit-REGI ster</span><span class="sxs-lookup"><span data-stu-id="b4569-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="b4569-109">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="b4569-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="b4569-110">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="b4569-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="b4569-111">Elke matrix moet een lijst bevatten met ints die het qubits beschrijven dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b4569-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="b4569-112">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b4569-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b4569-113">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="b4569-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b4569-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4569-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b4569-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b4569-115">See Also</span></span>

- [<span data-ttu-id="b4569-116">Micro soft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="b4569-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)