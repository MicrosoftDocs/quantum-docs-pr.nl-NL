---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Bewerking ApplyPhaseLEOperationOnLE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: dacc52766cf72d2bd562b76fc4939f962133e9a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707564"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="72195-102">Bewerking ApplyPhaseLEOperationOnLE</span><span class="sxs-lookup"><span data-stu-id="72195-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="72195-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="72195-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="72195-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="72195-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="72195-105">Hiermee wordt een bewerking toegepast waarbij een <xref:microsoft.quantum.arithmetic.littleendian> registratie als invoer wordt gebruikt voor een doel register van het type <xref:microsoft.quantum.arithmetic.phaselittleendian> .</span><span class="sxs-lookup"><span data-stu-id="72195-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="72195-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="72195-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="72195-107">op: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72195-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="72195-108">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="72195-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="72195-109">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="72195-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="72195-110">Het REGI ster waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="72195-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="72195-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72195-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="72195-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="72195-112">Remarks</span></span>

<span data-ttu-id="72195-113">Het REGI ster wordt getransformeerd met `PhaseLittleEndian` behulp van <xref:microsoft.quantum.canon.qftle> en wordt vervolgens teruggekeerd naar de oorspronkelijke weer gave na de toepassing van `op` .</span><span class="sxs-lookup"><span data-stu-id="72195-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="72195-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="72195-114">See Also</span></span>

- [<span data-ttu-id="72195-115">Micro soft. Quantum. Canon. ApplyPhaseLEOperationonLEA</span><span class="sxs-lookup"><span data-stu-id="72195-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="72195-116">Micro soft. Quantum. Canon. ApplyPhaseLEOperationonLEA</span><span class="sxs-lookup"><span data-stu-id="72195-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="72195-117">Micro soft. Quantum. Canon. ApplyPhaseLEOperationonLECA</span><span class="sxs-lookup"><span data-stu-id="72195-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)