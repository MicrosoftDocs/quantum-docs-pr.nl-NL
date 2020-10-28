---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Bewerking InjectPi4YRotation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 8558767050c317661dfb490143fa3c8f4ea009e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702476"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="9cc9d-102">Bewerking InjectPi4YRotation</span><span class="sxs-lookup"><span data-stu-id="9cc9d-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="9cc9d-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="9cc9d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="9cc9d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9cc9d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9cc9d-105">Hiermee roteert u één Qubit door π/4 over de Y-as.</span><span class="sxs-lookup"><span data-stu-id="9cc9d-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="9cc9d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9cc9d-106">Description</span></span>

<span data-ttu-id="9cc9d-107">Voert een π/4-rotatie over `Y` .</span><span class="sxs-lookup"><span data-stu-id="9cc9d-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="9cc9d-108">De rotatie wordt uitgevoerd door een magische status te gebruiken; dat wil zeggen, een kopie van de status $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} .</span><span class="sxs-lookup"><span data-stu-id="9cc9d-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="9cc9d-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9cc9d-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9cc9d-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="9cc9d-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="9cc9d-111">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9cc9d-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9cc9d-112">Een Qubit die moet worden gedraaid over $Y $ door $ \pi/$4.</span><span class="sxs-lookup"><span data-stu-id="9cc9d-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="9cc9d-113">Magic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9cc9d-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9cc9d-114">Een Qubit in eerste instantie in de status Magic.</span><span class="sxs-lookup"><span data-stu-id="9cc9d-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="9cc9d-115">De volgende toepassing van deze bewerking `magic` wordt geretourneerd naar de $ \ket {0} $-status.</span><span class="sxs-lookup"><span data-stu-id="9cc9d-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9cc9d-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9cc9d-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9cc9d-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9cc9d-117">Remarks</span></span>

<span data-ttu-id="9cc9d-118">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="9cc9d-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="9cc9d-119">en</span><span class="sxs-lookup"><span data-stu-id="9cc9d-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="9cc9d-120">Met deze bewerking `Adjoint` wordt de functor ondersteund. in dat geval wordt dezelfde Magic-status gebruikt, maar het effect op de gegevens Qubit is $-\ Pi/4 $ $Y $-Rotation.</span><span class="sxs-lookup"><span data-stu-id="9cc9d-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>