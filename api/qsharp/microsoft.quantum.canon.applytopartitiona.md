---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Bewerking ApplyToPartitionA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: f8f773e9fc3c18467185f9717a235649be8b385a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841290"
---
# <a name="applytopartitiona-operation"></a><span data-ttu-id="059f8-102">Bewerking ApplyToPartitionA</span><span class="sxs-lookup"><span data-stu-id="059f8-102">ApplyToPartitionA operation</span></span>

<span data-ttu-id="059f8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="059f8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="059f8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="059f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="059f8-105">Hiermee wordt een paar bewerkingen toegepast op een bepaalde partitie van een REGI ster in twee delen.</span><span class="sxs-lookup"><span data-stu-id="059f8-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="059f8-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="059f8-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="059f8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="059f8-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="059f8-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="059f8-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="059f8-109">Het paar bewerkingen dat moet worden toegepast op de opgegeven partitie.</span><span class="sxs-lookup"><span data-stu-id="059f8-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="059f8-110">numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="059f8-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="059f8-111">Het aantal qubits van het doel dat in het eerste deel van de partitie moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="059f8-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="059f8-112">De resterende qubits vormt het tweede deel van de partitie.</span><span class="sxs-lookup"><span data-stu-id="059f8-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="059f8-113">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="059f8-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="059f8-114">Een REGI ster van qubits die worden gepartitioneerd en worden uitgevoerd door de opgegeven twee bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="059f8-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="059f8-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="059f8-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="059f8-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="059f8-116">See Also</span></span>

- [<span data-ttu-id="059f8-117">Micro soft. Quantum. Canon. ApplyToPartition</span><span class="sxs-lookup"><span data-stu-id="059f8-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)