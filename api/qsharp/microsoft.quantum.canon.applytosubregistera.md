---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Bewerking ApplyToSubregisterA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7a5ae78edcda363f21cadaaed5cb273d35cb60cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841233"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="10290-102">Bewerking ApplyToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="10290-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="10290-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="10290-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="10290-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="10290-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="10290-105">Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.</span><span class="sxs-lookup"><span data-stu-id="10290-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="10290-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="10290-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="10290-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="10290-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="10290-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="10290-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="10290-109">Bewerking die moet worden toegepast op de subregister.</span><span class="sxs-lookup"><span data-stu-id="10290-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="10290-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="10290-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="10290-111">De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="10290-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="10290-112">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="10290-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="10290-113">Meld u aan waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="10290-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10290-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10290-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="10290-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="10290-115">See Also</span></span>

- [<span data-ttu-id="10290-116">Micro soft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="10290-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)