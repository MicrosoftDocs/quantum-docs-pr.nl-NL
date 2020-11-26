---
uid: Microsoft.Quantum.Intrinsic.S
title: S-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198449"
---
# <a name="s-operation"></a><span data-ttu-id="a37bb-102">S-bewerking</span><span class="sxs-lookup"><span data-stu-id="a37bb-102">S operation</span></span>

<span data-ttu-id="a37bb-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a37bb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a37bb-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a37bb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a37bb-105">De S-poort wordt toegepast op één Qubit.</span><span class="sxs-lookup"><span data-stu-id="a37bb-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a37bb-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a37bb-106">Description</span></span>

<span data-ttu-id="a37bb-107">Deze bewerking kan worden gesimuleerd door de unitary matrix \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="a37bb-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="a37bb-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a37bb-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="a37bb-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="a37bb-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="a37bb-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a37bb-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a37bb-111">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a37bb-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a37bb-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a37bb-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

