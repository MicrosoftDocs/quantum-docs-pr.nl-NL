---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Bewerking MAJ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846551"
---
# <a name="maj-operation"></a><span data-ttu-id="9675d-102">Bewerking MAJ</span><span class="sxs-lookup"><span data-stu-id="9675d-102">MAJ operation</span></span>

<span data-ttu-id="9675d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9675d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9675d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9675d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9675d-105">Dit past de in-place meerderheids bewerking toe op 3 qubits.</span><span class="sxs-lookup"><span data-stu-id="9675d-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="9675d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9675d-106">Description</span></span>

<span data-ttu-id="9675d-107">Als we de status van de doel-Qubit als $ \ket{z} $ aanduiden en de invoer status van de invoer qubits als $ \ket{x} $ en $ \ket{y} $, voert deze bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="9675d-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="9675d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9675d-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="9675d-109">input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9675d-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9675d-110">De eerste invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="9675d-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="9675d-111">input1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9675d-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9675d-112">De tweede invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="9675d-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9675d-113">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9675d-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9675d-114">Een Qubit waarop de functie meerderheid wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="9675d-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9675d-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9675d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

