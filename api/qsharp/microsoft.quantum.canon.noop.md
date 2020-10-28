---
uid: Microsoft.Quantum.Canon.NoOp
title: Bewerking Nooperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703947"
---
# <a name="noop-operation"></a><span data-ttu-id="c436f-102">Bewerking Nooperation</span><span class="sxs-lookup"><span data-stu-id="c436f-102">NoOp operation</span></span>

<span data-ttu-id="c436f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c436f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c436f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c436f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c436f-105">Hiermee wordt de identiteits bewerking (geen-op) uitgevoerd op een argument.</span><span class="sxs-lookup"><span data-stu-id="c436f-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="c436f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c436f-106">Description</span></span>

<span data-ttu-id="c436f-107">Met deze bewerking wordt een waarde van elk type gebruikt en gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="c436f-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="c436f-108">Dit kan handig zijn wanneer een invoer van een bewerkings type wordt verwacht, maar er geen actie moet worden ondernomen.</span><span class="sxs-lookup"><span data-stu-id="c436f-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="c436f-109">Als bijvoorbeeld een bepaalde fout correctie Syndrome aangeeft dat er geen fout is opgetreden, `NoOp<Qubit[]>` kan de juiste herstel procedure zijn.</span><span class="sxs-lookup"><span data-stu-id="c436f-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="c436f-110">Als een bewerking een status voorbereidings procedure als invoer verwacht, `NoOp<Qubit[]>` kan deze ook worden gebruikt om de status te voorbereiden $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="c436f-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="c436f-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="c436f-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="c436f-112">invoer: 'T</span><span class="sxs-lookup"><span data-stu-id="c436f-112">input : 'T</span></span>

<span data-ttu-id="c436f-113">Een waarde die moet worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="c436f-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c436f-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c436f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c436f-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c436f-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c436f-116">T</span><span class="sxs-lookup"><span data-stu-id="c436f-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="c436f-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c436f-117">Remarks</span></span>

<span data-ttu-id="c436f-118">In bijna alle gevallen moet de para meter type `NoOp` expliciet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c436f-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="c436f-119">`NoOp<Qubit>`Is bijvoorbeeld gelijk aan <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="c436f-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="c436f-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c436f-120">See Also</span></span>

- [<span data-ttu-id="c436f-121">Micro soft. Quantum. intrinsiek. Ik</span><span class="sxs-lookup"><span data-stu-id="c436f-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)