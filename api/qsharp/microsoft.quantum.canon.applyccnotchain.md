---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Bewerking ApplyCCNOTChain
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 53fdd59b06d542494647acb665f248fc18de93d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845144"
---
# <a name="applyccnotchain-operation"></a><span data-ttu-id="deb8e-102">Bewerking ApplyCCNOTChain</span><span class="sxs-lookup"><span data-stu-id="deb8e-102">ApplyCCNOTChain operation</span></span>

<span data-ttu-id="deb8e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="deb8e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="deb8e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="deb8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="deb8e-105">Hiermee wordt een trapsgewijs aantal CCNOT-poorten geïmplementeerd dat wordt beheerd op overeenkomstige bits van twee Qubit-registers, op de volgende Qubit van een van de registers.</span><span class="sxs-lookup"><span data-stu-id="deb8e-105">Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers.</span></span>
<span data-ttu-id="deb8e-106">Vanaf de qubits op positie 0 in beide registers als besturings elementen, wordt CCNOT toegepast op de Qubit op positie 1 van het doel register en vervolgens beheerd door de qubits op positie 1 op de Qubit op positie 2 in het doel register, enzovoort, eindigend met een actie op de doel-Qubit op positie `Length(nQubits)-1` .</span><span class="sxs-lookup"><span data-stu-id="deb8e-106">Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.</span></span>

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="deb8e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="deb8e-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="deb8e-108">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="deb8e-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="deb8e-109">Qubit-REGI ster, alleen gebruikt voor besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="deb8e-109">Qubit register, only used for controls.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="deb8e-110">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="deb8e-110">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="deb8e-111">Qubit-REGI ster, gebruikt voor besturings elementen en als doel.</span><span class="sxs-lookup"><span data-stu-id="deb8e-111">Qubit register, used for controls and as target.</span></span>



## <a name="output--unit"></a><span data-ttu-id="deb8e-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="deb8e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="deb8e-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="deb8e-113">Remarks</span></span>

<span data-ttu-id="deb8e-114">Het REGI ster van de doel-Qubit moet één Qubit meer dan het andere REGI ster hebben.</span><span class="sxs-lookup"><span data-stu-id="deb8e-114">The target qubit register must have one qubit more than the other register.</span></span>