---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Bewerking ApplyControlledOnBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 6947d2dbdec4cfbb592143024a7c8ccd53a32029
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219070"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="ea2d2-102">Bewerking ApplyControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="ea2d2-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="ea2d2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ea2d2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ea2d2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea2d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea2d2-105">Hiermee wordt een unitary-bewerking op het doel register toegepast, gecontroleerd op een status die is opgegeven door een opgegeven bitmasker.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ea2d2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ea2d2-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="ea2d2-107">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="ea2d2-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="ea2d2-108">De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="ea2d2-109">Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="ea2d2-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ea2d2-110">De unitary-bewerking die moet worden toegepast op het doel register.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="ea2d2-111">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ea2d2-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ea2d2-112">Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .</span><span class="sxs-lookup"><span data-stu-id="ea2d2-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="ea2d2-113">targetRegister: 'T</span><span class="sxs-lookup"><span data-stu-id="ea2d2-113">targetRegister : 'T</span></span>

<span data-ttu-id="ea2d2-114">Het doel register dat moet worden door gegeven `oracle` als invoer.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ea2d2-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea2d2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ea2d2-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ea2d2-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ea2d2-117">T</span><span class="sxs-lookup"><span data-stu-id="ea2d2-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="ea2d2-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ea2d2-118">Remarks</span></span>

<span data-ttu-id="ea2d2-119">Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="ea2d2-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="ea2d2-120">Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="ea2d2-121">`bits = [0,1,0,0,1]`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>