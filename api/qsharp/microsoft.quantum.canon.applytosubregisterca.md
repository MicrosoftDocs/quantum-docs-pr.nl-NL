---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Bewerking ApplyToSubregisterCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: a5ebfb17b1e66bd509f3a562f852986c83d0fef0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208003"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="a3cb8-102">Bewerking ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="a3cb8-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="a3cb8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a3cb8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a3cb8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3cb8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3cb8-105">Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.</span><span class="sxs-lookup"><span data-stu-id="a3cb8-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="a3cb8-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="a3cb8-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a3cb8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="a3cb8-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="a3cb8-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="a3cb8-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a3cb8-109">Bewerking die moet worden toegepast op de subregister.</span><span class="sxs-lookup"><span data-stu-id="a3cb8-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="a3cb8-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a3cb8-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a3cb8-111">De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a3cb8-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a3cb8-112">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a3cb8-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a3cb8-113">Meld u aan waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="a3cb8-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a3cb8-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3cb8-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="a3cb8-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a3cb8-115">See Also</span></span>

- [<span data-ttu-id="a3cb8-116">Micro soft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="a3cb8-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)