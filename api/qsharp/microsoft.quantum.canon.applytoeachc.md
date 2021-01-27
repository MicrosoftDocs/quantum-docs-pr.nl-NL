---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Bewerking ApplyToEachC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: b8b51e1c8d52c140c3ca1e5a54d0bd4cf4873046
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850843"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="7625e-102">Bewerking ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="7625e-102">ApplyToEachC operation</span></span>

<span data-ttu-id="7625e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7625e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7625e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7625e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7625e-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="7625e-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="7625e-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="7625e-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="7625e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="7625e-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="7625e-108">singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="7625e-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7625e-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="7625e-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="7625e-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="7625e-110">register : 'T[]</span></span>

<span data-ttu-id="7625e-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="7625e-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7625e-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7625e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7625e-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7625e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7625e-114">T</span><span class="sxs-lookup"><span data-stu-id="7625e-114">'T</span></span>

<span data-ttu-id="7625e-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="7625e-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="7625e-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7625e-116">Example</span></span>

<span data-ttu-id="7625e-117">Een Qubit $ \ket{+} $-status voorbereiden:</span><span class="sxs-lookup"><span data-stu-id="7625e-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="7625e-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7625e-118">See Also</span></span>

- [<span data-ttu-id="7625e-119">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="7625e-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)