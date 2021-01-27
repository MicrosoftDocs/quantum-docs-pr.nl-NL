---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Bewerking ApplyToSubregisterCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9f24c3ca9b152cf9bbf81e59b86f83a0ab459031
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841212"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="1e187-102">Bewerking ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="1e187-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="1e187-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1e187-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1e187-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e187-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e187-105">Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.</span><span class="sxs-lookup"><span data-stu-id="1e187-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="1e187-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="1e187-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1e187-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1e187-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="1e187-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="1e187-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1e187-109">Bewerking die moet worden toegepast op de subregister.</span><span class="sxs-lookup"><span data-stu-id="1e187-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="1e187-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1e187-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1e187-111">De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="1e187-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="1e187-112">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1e187-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1e187-113">Meld u aan waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="1e187-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1e187-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e187-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1e187-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1e187-115">See Also</span></span>

- [<span data-ttu-id="1e187-116">Micro soft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="1e187-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)