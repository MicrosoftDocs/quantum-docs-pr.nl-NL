---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEC
title: Bewerking ApplyLEOperationOnPhaseLEC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEC
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 6accddf4f46c0939c418e164ccb153a8fc6e358d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707612"
---
# <a name="applyleoperationonphaselec-operation"></a><span data-ttu-id="94009-102">Bewerking ApplyLEOperationOnPhaseLEC</span><span class="sxs-lookup"><span data-stu-id="94009-102">ApplyLEOperationOnPhaseLEC operation</span></span>

<span data-ttu-id="94009-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="94009-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="94009-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="94009-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="94009-105">Hiermee wordt een bewerking toegepast waarbij een <xref:microsoft.quantum.arithmetic.phaselittleendian> registratie als invoer wordt gebruikt voor een doel register van het type <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="94009-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="94009-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="94009-106">Input</span></span>

### <a name="op--littleendian--unit-ctl"></a><span data-ttu-id="94009-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) -CTL</span><span class="sxs-lookup"><span data-stu-id="94009-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="94009-108">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="94009-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="94009-109">doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="94009-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="94009-110">Het REGI ster waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="94009-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="94009-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="94009-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="94009-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="94009-112">Remarks</span></span>

<span data-ttu-id="94009-113">Het REGI ster wordt getransformeerd met `LittleEndian` behulp van <xref:microsoft.quantum.canon.qftle> en wordt vervolgens teruggekeerd naar de oorspronkelijke weer gave na de toepassing van `op` .</span><span class="sxs-lookup"><span data-stu-id="94009-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="94009-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="94009-114">See Also</span></span>

- [<span data-ttu-id="94009-115">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLE</span><span class="sxs-lookup"><span data-stu-id="94009-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="94009-116">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLEA</span><span class="sxs-lookup"><span data-stu-id="94009-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="94009-117">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLECA</span><span class="sxs-lookup"><span data-stu-id="94009-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)