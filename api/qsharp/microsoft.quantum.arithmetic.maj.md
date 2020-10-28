---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Bewerking MAJ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707205"
---
# <a name="maj-operation"></a><span data-ttu-id="dfd62-102">Bewerking MAJ</span><span class="sxs-lookup"><span data-stu-id="dfd62-102">MAJ operation</span></span>

<span data-ttu-id="dfd62-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dfd62-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dfd62-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dfd62-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dfd62-105">Dit past de in-place meerderheids bewerking toe op 3 qubits.</span><span class="sxs-lookup"><span data-stu-id="dfd62-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="dfd62-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dfd62-106">Description</span></span>

<span data-ttu-id="dfd62-107">Als we de status van de doel-Qubit als $ \ket{z} $ aanduiden en de invoer status van de invoer qubits als $ \ket{x} $ en $ \ket{y} $, voert deze bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="dfd62-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="dfd62-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="dfd62-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="dfd62-109">input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dfd62-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dfd62-110">De eerste invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="dfd62-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="dfd62-111">input1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dfd62-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dfd62-112">De tweede invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="dfd62-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="dfd62-113">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dfd62-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dfd62-114">Een Qubit waarop de functie meerderheid wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="dfd62-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfd62-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfd62-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

