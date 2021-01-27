---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Bewerking ApplyToPartition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: a0dc3453e7501816132569869e858418d5f3f4e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850546"
---
# <a name="applytopartition-operation"></a><span data-ttu-id="73752-102">Bewerking ApplyToPartition</span><span class="sxs-lookup"><span data-stu-id="73752-102">ApplyToPartition operation</span></span>

<span data-ttu-id="73752-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="73752-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="73752-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73752-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73752-105">Hiermee wordt een paar bewerkingen toegepast op een bepaalde partitie van een REGI ster in twee delen.</span><span class="sxs-lookup"><span data-stu-id="73752-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="73752-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="73752-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="73752-107">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73752-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="73752-108">Het paar bewerkingen dat moet worden toegepast op de opgegeven partitie.</span><span class="sxs-lookup"><span data-stu-id="73752-108">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="73752-109">numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73752-109">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73752-110">Het aantal qubits van het doel dat in het eerste deel van de partitie moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="73752-110">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="73752-111">De resterende qubits vormt het tweede deel van de partitie.</span><span class="sxs-lookup"><span data-stu-id="73752-111">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="73752-112">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="73752-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="73752-113">Een REGI ster van qubits die worden gepartitioneerd en worden uitgevoerd door de opgegeven twee bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="73752-113">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="73752-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73752-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="73752-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="73752-115">See Also</span></span>

- [<span data-ttu-id="73752-116">Micro soft. Quantum. Canon. ApplyToPartitionA</span><span class="sxs-lookup"><span data-stu-id="73752-116">Microsoft.Quantum.Canon.ApplyToPartitionA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [<span data-ttu-id="73752-117">Micro soft. Quantum. Canon. ApplyToPartitionC</span><span class="sxs-lookup"><span data-stu-id="73752-117">Microsoft.Quantum.Canon.ApplyToPartitionC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [<span data-ttu-id="73752-118">Micro soft. Quantum. Canon. ApplyToPartitionCA</span><span class="sxs-lookup"><span data-stu-id="73752-118">Microsoft.Quantum.Canon.ApplyToPartitionCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)