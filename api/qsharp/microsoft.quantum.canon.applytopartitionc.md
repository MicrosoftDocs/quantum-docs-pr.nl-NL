---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Bewerking ApplyToPartitionC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850531"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="9f2af-102">Bewerking ApplyToPartitionC</span><span class="sxs-lookup"><span data-stu-id="9f2af-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="9f2af-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9f2af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9f2af-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9f2af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9f2af-105">Hiermee wordt een paar bewerkingen toegepast op een bepaalde partitie van een REGI ster in twee delen.</span><span class="sxs-lookup"><span data-stu-id="9f2af-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="9f2af-106">De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="9f2af-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="9f2af-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="9f2af-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="9f2af-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9f2af-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9f2af-109">Het paar bewerkingen dat moet worden toegepast op de opgegeven partitie.</span><span class="sxs-lookup"><span data-stu-id="9f2af-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="9f2af-110">numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f2af-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f2af-111">Het aantal qubits van het doel dat in het eerste deel van de partitie moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="9f2af-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="9f2af-112">De resterende qubits vormt het tweede deel van de partitie.</span><span class="sxs-lookup"><span data-stu-id="9f2af-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9f2af-113">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9f2af-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9f2af-114">Een REGI ster van qubits die worden gepartitioneerd en worden uitgevoerd door de opgegeven twee bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="9f2af-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f2af-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f2af-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9f2af-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9f2af-116">See Also</span></span>

- [<span data-ttu-id="9f2af-117">Micro soft. Quantum. Canon. ApplyToPartition</span><span class="sxs-lookup"><span data-stu-id="9f2af-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)