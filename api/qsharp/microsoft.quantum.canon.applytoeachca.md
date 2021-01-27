---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Bewerking ApplyToEachCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841478"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="f87c8-102">Bewerking ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="f87c8-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="f87c8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f87c8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f87c8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f87c8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f87c8-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f87c8-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f87c8-106">De aanpassings functie `CA` geeft aan dat de bewerking met één qubit kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="f87c8-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f87c8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f87c8-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="f87c8-108">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="f87c8-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f87c8-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="f87c8-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f87c8-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="f87c8-110">register : 'T[]</span></span>

<span data-ttu-id="f87c8-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f87c8-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f87c8-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f87c8-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f87c8-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f87c8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f87c8-114">T</span><span class="sxs-lookup"><span data-stu-id="f87c8-114">'T</span></span>

<span data-ttu-id="f87c8-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="f87c8-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="f87c8-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f87c8-116">Example</span></span>

<span data-ttu-id="f87c8-117">Een Qubit $ \ket{+} $-status voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="f87c8-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="f87c8-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f87c8-118">See Also</span></span>

- [<span data-ttu-id="f87c8-119">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="f87c8-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)