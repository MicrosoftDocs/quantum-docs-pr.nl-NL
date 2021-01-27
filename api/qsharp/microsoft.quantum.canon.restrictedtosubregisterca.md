---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: De functie RestrictedToSubregisterCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9b1c8a6d1c843fb0533af16aafc4b3ca2ba2f0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852172"
---
# <a name="restrictedtosubregisterca-function"></a><span data-ttu-id="373d2-102">De functie RestrictedToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="373d2-102">RestrictedToSubregisterCA function</span></span>

<span data-ttu-id="373d2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="373d2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="373d2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="373d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="373d2-105">Hiermee wordt een bewerking beperkt tot een matrix van indices van een REGI ster, dat wil zeggen een subregistratie.</span><span class="sxs-lookup"><span data-stu-id="373d2-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="373d2-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="373d2-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="373d2-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="373d2-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="373d2-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="373d2-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="373d2-109">De bewerking die moet worden beperkt tot een subjournaal.</span><span class="sxs-lookup"><span data-stu-id="373d2-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="373d2-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="373d2-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="373d2-111">Matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt beperkt.</span><span class="sxs-lookup"><span data-stu-id="373d2-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="373d2-112">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="373d2-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="373d2-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="373d2-113">See Also</span></span>

- [<span data-ttu-id="373d2-114">Micro soft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="373d2-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)