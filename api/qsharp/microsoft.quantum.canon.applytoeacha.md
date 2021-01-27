---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Bewerking ApplyToEachA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844606"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="f20f9-102">Bewerking ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="f20f9-102">ApplyToEachA operation</span></span>

<span data-ttu-id="f20f9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f20f9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f20f9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f20f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f20f9-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f20f9-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f20f9-106">De aanpassings functie `A` geeft aan dat de bewerking met één Qubit adjointable is.</span><span class="sxs-lookup"><span data-stu-id="f20f9-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f20f9-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f20f9-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj"></a><span data-ttu-id="f20f9-108">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="f20f9-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f20f9-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="f20f9-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f20f9-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="f20f9-110">register : 'T[]</span></span>

<span data-ttu-id="f20f9-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f20f9-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f20f9-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f20f9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f20f9-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f20f9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f20f9-114">T</span><span class="sxs-lookup"><span data-stu-id="f20f9-114">'T</span></span>

<span data-ttu-id="f20f9-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="f20f9-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="f20f9-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f20f9-116">Example</span></span>

<span data-ttu-id="f20f9-117">Een Qubit $ \ket{+} $-status voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="f20f9-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="f20f9-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f20f9-118">See Also</span></span>

- [<span data-ttu-id="f20f9-119">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="f20f9-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)