---
uid: Microsoft.Quantum.Canon.NoOp
title: Bewerking Nooperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 45f3c8c9d4bae8ac8f7f60c4e4f8ead5d92e7c00
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852397"
---
# <a name="noop-operation"></a><span data-ttu-id="e411d-102">Bewerking Nooperation</span><span class="sxs-lookup"><span data-stu-id="e411d-102">NoOp operation</span></span>

<span data-ttu-id="e411d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e411d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e411d-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e411d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e411d-105">Hiermee wordt de identiteits bewerking (geen-op) uitgevoerd op een argument.</span><span class="sxs-lookup"><span data-stu-id="e411d-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e411d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e411d-106">Description</span></span>

<span data-ttu-id="e411d-107">Met deze bewerking wordt een waarde van elk type gebruikt en gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="e411d-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="e411d-108">Dit kan handig zijn wanneer een invoer van een bewerkings type wordt verwacht, maar er geen actie moet worden ondernomen.</span><span class="sxs-lookup"><span data-stu-id="e411d-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="e411d-109">Als bijvoorbeeld een bepaalde fout correctie Syndrome aangeeft dat er geen fout is opgetreden, `NoOp<Qubit[]>` kan de juiste herstel procedure zijn.</span><span class="sxs-lookup"><span data-stu-id="e411d-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="e411d-110">Als een bewerking een status voorbereidings procedure als invoer verwacht, `NoOp<Qubit[]>` kan deze ook worden gebruikt om de status te voorbereiden $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="e411d-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="e411d-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="e411d-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="e411d-112">invoer: 'T</span><span class="sxs-lookup"><span data-stu-id="e411d-112">input : 'T</span></span>

<span data-ttu-id="e411d-113">Een waarde die moet worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="e411d-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e411d-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e411d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e411d-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e411d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e411d-116">T</span><span class="sxs-lookup"><span data-stu-id="e411d-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="e411d-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e411d-117">Remarks</span></span>

<span data-ttu-id="e411d-118">In bijna alle gevallen moet de para meter type `NoOp` expliciet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e411d-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="e411d-119">`NoOp<Qubit>`Is bijvoorbeeld gelijk aan <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="e411d-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="e411d-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e411d-120">See Also</span></span>

- [<span data-ttu-id="e411d-121">Micro soft. Quantum. intrinsiek. Ik</span><span class="sxs-lookup"><span data-stu-id="e411d-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)