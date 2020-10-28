---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Bewerking ApplyDeltaParity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708641"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="db30b-102">Bewerking ApplyDeltaParity</span><span class="sxs-lookup"><span data-stu-id="db30b-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="db30b-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="db30b-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="db30b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="db30b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="db30b-105">Berekent het verschil in pariteit tussen een vorige PQRS... voor waarden en de volgende PQRS... mandaat.</span><span class="sxs-lookup"><span data-stu-id="db30b-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="db30b-106">Dit verschil wordt berekend op een hulp Qubit.</span><span class="sxs-lookup"><span data-stu-id="db30b-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="db30b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="db30b-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="db30b-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="db30b-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="db30b-109">Lijst met indexen voor vorige PQRS... inzake.</span><span class="sxs-lookup"><span data-stu-id="db30b-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="db30b-110">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="db30b-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="db30b-111">Lijst met indexen voor de volgende PQRS... inzake.</span><span class="sxs-lookup"><span data-stu-id="db30b-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="db30b-112">AUX: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="db30b-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="db30b-113">Hulp Qubit waarop de resultaten van de pariteits berekening worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="db30b-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="db30b-114">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="db30b-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="db30b-115">Qubit verwerkt door alle PQRS... inzake.</span><span class="sxs-lookup"><span data-stu-id="db30b-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="db30b-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="db30b-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="db30b-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="db30b-117">Remarks</span></span>

<span data-ttu-id="db30b-118">Hierbij wordt ervan uitgegaan dat de indices P < Q < R < S <... voor zowel prevPQ als nextPQ.</span><span class="sxs-lookup"><span data-stu-id="db30b-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>