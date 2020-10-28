---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: De functie RestrictedToSubregisterA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: d45c43caed35df8fb89d9d38e540faf5a21ea064
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703851"
---
# <a name="restrictedtosubregistera-function"></a><span data-ttu-id="17f1d-102">De functie RestrictedToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="17f1d-102">RestrictedToSubregisterA function</span></span>

<span data-ttu-id="17f1d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="17f1d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="17f1d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17f1d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17f1d-105">Hiermee wordt een bewerking beperkt tot een matrix van indices van een REGI ster, dat wil zeggen een subregistratie.</span><span class="sxs-lookup"><span data-stu-id="17f1d-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="17f1d-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="17f1d-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="17f1d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="17f1d-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="17f1d-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="17f1d-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="17f1d-109">De bewerking die moet worden beperkt tot een subjournaal.</span><span class="sxs-lookup"><span data-stu-id="17f1d-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="17f1d-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="17f1d-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="17f1d-111">Matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt beperkt.</span><span class="sxs-lookup"><span data-stu-id="17f1d-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-adj"></a><span data-ttu-id="17f1d-112">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="17f1d-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>



## <a name="see-also"></a><span data-ttu-id="17f1d-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="17f1d-113">See Also</span></span>

- [<span data-ttu-id="17f1d-114">Micro soft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="17f1d-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)