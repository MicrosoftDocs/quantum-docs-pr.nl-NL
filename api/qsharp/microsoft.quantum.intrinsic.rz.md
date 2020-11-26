---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Bewerking RZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: d637abf3562eb60705da517467939dc588229c39
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198619"
---
# <a name="rz-operation"></a><span data-ttu-id="c52ea-102">Bewerking RZ</span><span class="sxs-lookup"><span data-stu-id="c52ea-102">Rz operation</span></span>

<span data-ttu-id="c52ea-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c52ea-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c52ea-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c52ea-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c52ea-105">Past een rotatie over de $z $-axis op een bepaalde hoek toe.</span><span class="sxs-lookup"><span data-stu-id="c52ea-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="c52ea-106">\begin{align} R_z (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \theta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="c52ea-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="c52ea-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="c52ea-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c52ea-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c52ea-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="c52ea-109">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c52ea-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c52ea-110">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="c52ea-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="c52ea-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c52ea-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c52ea-112">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c52ea-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c52ea-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c52ea-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c52ea-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c52ea-114">Remarks</span></span>

<span data-ttu-id="c52ea-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="c52ea-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```