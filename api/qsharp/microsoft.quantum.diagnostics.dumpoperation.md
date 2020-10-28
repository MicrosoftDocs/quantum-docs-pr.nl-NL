---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Bewerking DumpOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702705"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="99e85-102">Bewerking DumpOperation</span><span class="sxs-lookup"><span data-stu-id="99e85-102">DumpOperation operation</span></span>

<span data-ttu-id="99e85-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="99e85-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="99e85-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="99e85-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="99e85-105">Op basis van een bewerking worden diagnostische gegevens weer gegeven over de bewerking die beschikbaar is gemaakt door het huidige doel van de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="99e85-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="99e85-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="99e85-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="99e85-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99e85-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99e85-108">Het aantal qubits waarop de opgegeven bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="99e85-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit-adj"></a><span data-ttu-id="99e85-109">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="99e85-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="99e85-110">De bewerking die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="99e85-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="99e85-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99e85-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="99e85-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="99e85-112">Remarks</span></span>

<span data-ttu-id="99e85-113">Het aanroepen van deze bewerking heeft geen waarneembaar effect van binnen Q #.</span><span class="sxs-lookup"><span data-stu-id="99e85-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="99e85-114">De exacte diagnostische gegevens die worden weer gegeven, zijn afhankelijk van de huidige uitvoer doel-en-Editor omgeving.</span><span class="sxs-lookup"><span data-stu-id="99e85-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="99e85-115">Als er bijvoorbeeld gebruik wordt gemaakt van de volledige Quantum-Simulator, wordt een unitary-matrix weer gegeven die wordt gebruikt om aan te duiden `op` .</span><span class="sxs-lookup"><span data-stu-id="99e85-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="99e85-116">Houd er rekening mee dat bij het uitvoeren van simulatoren die een globale fase ambiguïteit veroorzaken (bijvoorbeeld: de Full-State Simulator), geretourneerde representaties kunnen variëren tot een globale fase.</span><span class="sxs-lookup"><span data-stu-id="99e85-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="99e85-117">De volg orde van de weer gaven van rijen en kolommen matrix kan ook verschillen met de conventies die worden gebruikt door elke Simulator die deze bewerking ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="99e85-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>