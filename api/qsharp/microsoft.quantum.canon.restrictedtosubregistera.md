---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: De functie RestrictedToSubregisterA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c260a0e422d7ffb8137f6ac41e1cb398b2f4a2a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852185"
---
# <a name="restrictedtosubregistera-function"></a><span data-ttu-id="c4a2c-102">De functie RestrictedToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="c4a2c-102">RestrictedToSubregisterA function</span></span>

<span data-ttu-id="c4a2c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4a2c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4a2c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4a2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4a2c-105">Hiermee wordt een bewerking beperkt tot een matrix van indices van een REGI ster, dat wil zeggen een subregistratie.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="c4a2c-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="c4a2c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c4a2c-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="c4a2c-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c4a2c-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c4a2c-109">De bewerking die moet worden beperkt tot een subjournaal.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="c4a2c-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c4a2c-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c4a2c-111">Matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt beperkt.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-adj"></a><span data-ttu-id="c4a2c-112">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c4a2c-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>



## <a name="see-also"></a><span data-ttu-id="c4a2c-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c4a2c-113">See Also</span></span>

- [<span data-ttu-id="c4a2c-114">Micro soft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="c4a2c-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)