---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Bewerking RK
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 9966693eb7283e855f7b72e910aa3604d6c2bd61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706533"
---
# <a name="ry-operation"></a><span data-ttu-id="4c9cf-102">Bewerking RK</span><span class="sxs-lookup"><span data-stu-id="4c9cf-102">Ry operation</span></span>

<span data-ttu-id="4c9cf-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="4c9cf-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="4c9cf-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4c9cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4c9cf-105">Past een rotatie over de $y $-axis op een bepaalde hoek toe.</span><span class="sxs-lookup"><span data-stu-id="4c9cf-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="4c9cf-106">\begin{align} R_y (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_y/2} = \begin{bmatrix} \cos \frac{\theta} {2} &-\sin \frac{\theta} {2} \\ \\ \sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="4c9cf-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="4c9cf-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="4c9cf-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="4c9cf-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4c9cf-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="4c9cf-109">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4c9cf-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4c9cf-110">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="4c9cf-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="4c9cf-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4c9cf-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4c9cf-112">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4c9cf-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4c9cf-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c9cf-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4c9cf-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4c9cf-114">Remarks</span></span>

<span data-ttu-id="4c9cf-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="4c9cf-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```