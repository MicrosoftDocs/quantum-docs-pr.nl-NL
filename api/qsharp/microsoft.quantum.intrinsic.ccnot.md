---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Bewerking CCNOT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702140"
---
# <a name="ccnot-operation"></a><span data-ttu-id="ec49e-102">Bewerking CCNOT</span><span class="sxs-lookup"><span data-stu-id="ec49e-102">CCNOT operation</span></span>

<span data-ttu-id="ec49e-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ec49e-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ec49e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec49e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec49e-105">Past de CCNOT-poort (dubbele controle – niet) toe op drie qubits.</span><span class="sxs-lookup"><span data-stu-id="ec49e-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ec49e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ec49e-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="ec49e-107">control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ec49e-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ec49e-108">First Control Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="ec49e-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="ec49e-109">control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ec49e-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ec49e-110">Tweede besturings element Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="ec49e-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ec49e-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ec49e-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ec49e-112">Doel-Qubit voor de CCNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="ec49e-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec49e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec49e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ec49e-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ec49e-114">Remarks</span></span>

<span data-ttu-id="ec49e-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="ec49e-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```