---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Bewerking CCNOT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: a9186269a868c2ac9d2f15727a3b0ed1bfec3fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819034"
---
# <a name="ccnot-operation"></a><span data-ttu-id="9cfb2-102">Bewerking CCNOT</span><span class="sxs-lookup"><span data-stu-id="9cfb2-102">CCNOT operation</span></span>

<span data-ttu-id="9cfb2-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9cfb2-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9cfb2-105">Past de CCNOT-poort (dubbele controle – niet) toe op drie qubits.</span><span class="sxs-lookup"><span data-stu-id="9cfb2-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9cfb2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9cfb2-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="9cfb2-107">control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9cfb2-108">First Control Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="9cfb2-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="9cfb2-109">control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9cfb2-110">Tweede besturings element Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="9cfb2-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9cfb2-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9cfb2-112">Doel-Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="9cfb2-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9cfb2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9cfb2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9cfb2-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9cfb2-114">Remarks</span></span>

<span data-ttu-id="9cfb2-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="9cfb2-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```