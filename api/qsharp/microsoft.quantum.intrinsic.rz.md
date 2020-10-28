---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Bewerking RZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 954b0b097d4bffcb8047a9f0c8a4c28445653c5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707108"
---
# <a name="rz-operation"></a><span data-ttu-id="1139d-102">Bewerking RZ</span><span class="sxs-lookup"><span data-stu-id="1139d-102">Rz operation</span></span>

<span data-ttu-id="1139d-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="1139d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="1139d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1139d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1139d-105">Past een rotatie over de $z $-axis op een bepaalde hoek toe.</span><span class="sxs-lookup"><span data-stu-id="1139d-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="1139d-106">\begin{align} R_z (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \theta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="1139d-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="1139d-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="1139d-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="1139d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="1139d-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="1139d-109">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1139d-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1139d-110">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="1139d-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="1139d-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1139d-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1139d-112">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1139d-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1139d-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1139d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1139d-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1139d-114">Remarks</span></span>

<span data-ttu-id="1139d-115">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="1139d-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```