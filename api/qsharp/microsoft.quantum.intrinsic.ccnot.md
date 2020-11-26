---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Bewerking CCNOT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: 715796ddd915d80036933e3f1ceefa97aa62cecf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212474"
---
# <a name="ccnot-operation"></a><span data-ttu-id="855b3-102">Bewerking CCNOT</span><span class="sxs-lookup"><span data-stu-id="855b3-102">CCNOT operation</span></span>

<span data-ttu-id="855b3-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="855b3-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="855b3-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="855b3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="855b3-105">Past de CCNOT-poort (dubbele controle – niet) toe op drie qubits.</span><span class="sxs-lookup"><span data-stu-id="855b3-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="855b3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="855b3-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="855b3-107">control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="855b3-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="855b3-108">First Control Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="855b3-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="855b3-109">control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="855b3-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="855b3-110">Tweede besturings element Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="855b3-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="855b3-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="855b3-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="855b3-112">Doel-Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="855b3-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="855b3-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="855b3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="855b3-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="855b3-114">Remarks</span></span>

<span data-ttu-id="855b3-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="855b3-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```