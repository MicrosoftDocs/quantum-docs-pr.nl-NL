---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Bewerking RK
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 5a1f762aacca5c72dc8dbe450ab8e8a4aef12c69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198602"
---
# <a name="ry-operation"></a><span data-ttu-id="eb402-102">Bewerking RK</span><span class="sxs-lookup"><span data-stu-id="eb402-102">Ry operation</span></span>

<span data-ttu-id="eb402-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="eb402-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="eb402-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="eb402-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="eb402-105">Past een rotatie over de $y $-axis op een bepaalde hoek toe.</span><span class="sxs-lookup"><span data-stu-id="eb402-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="eb402-106">\begin{align} R_y (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_y/2} = \begin{bmatrix} \cos \frac{\theta} {2} &-\sin \frac{\theta} {2} \\ \\ \sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="eb402-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="eb402-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="eb402-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="eb402-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="eb402-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="eb402-109">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eb402-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eb402-110">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="eb402-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="eb402-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="eb402-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="eb402-112">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="eb402-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb402-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb402-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="eb402-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="eb402-114">Remarks</span></span>

<span data-ttu-id="eb402-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="eb402-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```