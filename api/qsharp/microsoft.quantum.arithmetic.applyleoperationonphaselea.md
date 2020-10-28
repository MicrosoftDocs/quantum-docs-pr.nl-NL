---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEA
title: Bewerking ApplyLEOperationOnPhaseLEA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 572c66b201b6d2c816017230527c70c1b3c83371
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707613"
---
# <a name="applyleoperationonphaselea-operation"></a><span data-ttu-id="6f285-102">Bewerking ApplyLEOperationOnPhaseLEA</span><span class="sxs-lookup"><span data-stu-id="6f285-102">ApplyLEOperationOnPhaseLEA operation</span></span>

<span data-ttu-id="6f285-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6f285-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6f285-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f285-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f285-105">Hiermee wordt een bewerking toegepast waarbij een <xref:microsoft.quantum.arithmetic.phaselittleendian> registratie als invoer wordt gebruikt voor een doel register van het type <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="6f285-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="6f285-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6f285-106">Input</span></span>

### <a name="op--littleendian--unit-adj"></a><span data-ttu-id="6f285-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="6f285-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6f285-108">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6f285-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="6f285-109">doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6f285-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="6f285-110">Het REGI ster waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="6f285-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6f285-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f285-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6f285-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6f285-112">Remarks</span></span>

<span data-ttu-id="6f285-113">Het REGI ster wordt getransformeerd met `LittleEndian` behulp van <xref:microsoft.quantum.canon.qftle> en wordt vervolgens teruggekeerd naar de oorspronkelijke weer gave na de toepassing van `op` .</span><span class="sxs-lookup"><span data-stu-id="6f285-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f285-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6f285-114">See Also</span></span>

- [<span data-ttu-id="6f285-115">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLE</span><span class="sxs-lookup"><span data-stu-id="6f285-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="6f285-116">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLEC</span><span class="sxs-lookup"><span data-stu-id="6f285-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [<span data-ttu-id="6f285-117">Micro soft. Quantum. Canon. ApplyLEOperationonPhaseLECA</span><span class="sxs-lookup"><span data-stu-id="6f285-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)