---
uid: Microsoft.Quantum.Intrinsic.R1
title: R1-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: 07cce580b50fef5664fdac32bb4fae0ba22d25e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849355"
---
# <a name="r1-operation"></a><span data-ttu-id="3de8e-102">R1-bewerking</span><span class="sxs-lookup"><span data-stu-id="3de8e-102">R1 operation</span></span>

<span data-ttu-id="3de8e-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="3de8e-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="3de8e-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3de8e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3de8e-105">Past een rotatie over de $ \ket {1} $-status toe op basis van een bepaalde hoek.</span><span class="sxs-lookup"><span data-stu-id="3de8e-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="3de8e-106">\begin{align} R_1 (\theta) \mathrel{: =} \operatorname{diag} (1, e ^ {i\theta}).</span><span class="sxs-lookup"><span data-stu-id="3de8e-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="3de8e-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="3de8e-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3de8e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="3de8e-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="3de8e-109">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3de8e-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3de8e-110">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="3de8e-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="3de8e-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3de8e-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3de8e-112">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="3de8e-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3de8e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3de8e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3de8e-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3de8e-114">Remarks</span></span>

<span data-ttu-id="3de8e-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="3de8e-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```