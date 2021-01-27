---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Bewerking ApplyToEach
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 61dda69751989ef8a98fa8fb01d832014ec4ad35
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844627"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="1881f-102">Bewerking ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="1881f-102">ApplyToEach operation</span></span>

<span data-ttu-id="1881f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1881f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1881f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1881f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1881f-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="1881f-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1881f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1881f-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="1881f-107">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1881f-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1881f-108">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="1881f-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1881f-109">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="1881f-109">register : 'T[]</span></span>

<span data-ttu-id="1881f-110">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1881f-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1881f-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1881f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1881f-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1881f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1881f-113">T</span><span class="sxs-lookup"><span data-stu-id="1881f-113">'T</span></span>

<span data-ttu-id="1881f-114">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="1881f-114">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="1881f-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1881f-115">Example</span></span>

<span data-ttu-id="1881f-116">Een Qubit $ \ket{+} $-status voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="1881f-116">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="1881f-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1881f-117">See Also</span></span>

- [<span data-ttu-id="1881f-118">Micro soft. Quantum. Canon. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="1881f-118">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="1881f-119">Micro soft. Quantum. Canon. ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="1881f-119">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="1881f-120">Micro soft. Quantum. Canon. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="1881f-120">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)