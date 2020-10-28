---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Bewerking ApplyToSubregisterCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 3eb210debf8980f057ed150f647d545f68734459
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704637"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="41a24-102">Bewerking ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="41a24-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="41a24-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="41a24-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="41a24-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41a24-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41a24-105">Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.</span><span class="sxs-lookup"><span data-stu-id="41a24-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="41a24-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="41a24-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="41a24-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="41a24-107">Input</span></span>

### <a name="op--qubit--unit-ctl--adj"></a><span data-ttu-id="41a24-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] = Ctl van> [Unit](xref:microsoft.quantum.lang-ref.unit) + ADJ</span><span class="sxs-lookup"><span data-stu-id="41a24-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="41a24-109">Bewerking die moet worden toegepast op de subregister.</span><span class="sxs-lookup"><span data-stu-id="41a24-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="41a24-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="41a24-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="41a24-111">De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="41a24-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="41a24-112">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="41a24-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="41a24-113">Meld u aan waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="41a24-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="41a24-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="41a24-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="41a24-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="41a24-115">See Also</span></span>

- [<span data-ttu-id="41a24-116">Micro soft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="41a24-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)