---
uid: Microsoft.Quantum.Intrinsic.T
title: T-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 868031386c95f65ae956b5e444c6d87d7ea0a697
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707100"
---
# <a name="t-operation"></a><span data-ttu-id="cb65a-102">T-bewerking</span><span class="sxs-lookup"><span data-stu-id="cb65a-102">T operation</span></span>

<span data-ttu-id="cb65a-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="cb65a-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="cb65a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cb65a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cb65a-105">Hiermee past u de T-poort toe op één Qubit.</span><span class="sxs-lookup"><span data-stu-id="cb65a-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="cb65a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="cb65a-106">Description</span></span>

<span data-ttu-id="cb65a-107">Deze bewerking kan worden gesimuleerd door de unitary matrix \begin{align} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="cb65a-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="cb65a-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="cb65a-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="cb65a-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="cb65a-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="cb65a-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cb65a-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cb65a-111">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="cb65a-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cb65a-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cb65a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

