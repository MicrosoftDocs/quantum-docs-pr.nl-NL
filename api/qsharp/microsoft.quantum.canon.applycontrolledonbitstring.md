---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Bewerking ApplyControlledOnBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705436"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="67c1b-102">Bewerking ApplyControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="67c1b-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="67c1b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="67c1b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="67c1b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67c1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67c1b-105">Hiermee wordt een unitary-bewerking op het doel register toegepast, gecontroleerd op een status die is opgegeven door een opgegeven bitmasker.</span><span class="sxs-lookup"><span data-stu-id="67c1b-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="67c1b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="67c1b-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="67c1b-107">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="67c1b-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="67c1b-108">De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.</span><span class="sxs-lookup"><span data-stu-id="67c1b-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="67c1b-109">Oracle: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="67c1b-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="67c1b-110">De unitary-bewerking die moet worden toegepast op het doel register.</span><span class="sxs-lookup"><span data-stu-id="67c1b-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="67c1b-111">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="67c1b-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="67c1b-112">Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .</span><span class="sxs-lookup"><span data-stu-id="67c1b-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="67c1b-113">targetRegister: 'T</span><span class="sxs-lookup"><span data-stu-id="67c1b-113">targetRegister : 'T</span></span>

<span data-ttu-id="67c1b-114">Het doel register dat moet worden door gegeven `oracle` als invoer.</span><span class="sxs-lookup"><span data-stu-id="67c1b-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="67c1b-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="67c1b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="67c1b-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="67c1b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67c1b-117">T</span><span class="sxs-lookup"><span data-stu-id="67c1b-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="67c1b-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="67c1b-118">Remarks</span></span>

<span data-ttu-id="67c1b-119">Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="67c1b-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="67c1b-120">Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.</span><span class="sxs-lookup"><span data-stu-id="67c1b-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="67c1b-121">`bits = [0,1,0,0,1]`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="67c1b-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>