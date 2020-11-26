---
uid: Microsoft.Quantum.Intrinsic.T
title: T-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 352ef2c1b15a46dea85c420fc6f1cfab0382e73a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198398"
---
# <a name="t-operation"></a><span data-ttu-id="7b480-102">T-bewerking</span><span class="sxs-lookup"><span data-stu-id="7b480-102">T operation</span></span>

<span data-ttu-id="7b480-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="7b480-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="7b480-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7b480-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7b480-105">Hiermee past u de T-poort toe op één Qubit.</span><span class="sxs-lookup"><span data-stu-id="7b480-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="7b480-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7b480-106">Description</span></span>

<span data-ttu-id="7b480-107">Deze bewerking kan worden gesimuleerd door de unitary matrix \begin{align} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="7b480-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="7b480-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="7b480-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="7b480-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="7b480-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="7b480-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7b480-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7b480-111">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="7b480-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7b480-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7b480-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

