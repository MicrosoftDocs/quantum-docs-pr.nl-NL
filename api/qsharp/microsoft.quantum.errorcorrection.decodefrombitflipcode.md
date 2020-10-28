---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Bewerking DecodeFromBitFlipCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702543"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="92e9e-102">Bewerking DecodeFromBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="92e9e-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="92e9e-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="92e9e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="92e9e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92e9e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92e9e-105">Decoderen van de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-Flip code.</span><span class="sxs-lookup"><span data-stu-id="92e9e-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="92e9e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="92e9e-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="92e9e-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="92e9e-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="92e9e-108">Een code blok van de bits-Flip-code.</span><span class="sxs-lookup"><span data-stu-id="92e9e-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="92e9e-109">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="92e9e-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="92e9e-110">Een tuple van de gegevens die zijn gecodeerd in het logische REGI ster en de hulp qubits die wordt gebruikt om de Syndrome aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="92e9e-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="92e9e-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="92e9e-111">See Also</span></span>

- [<span data-ttu-id="92e9e-112">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="92e9e-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="92e9e-113">Micro soft. Quantum. ErrorCorrection. EncodeIntoBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="92e9e-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)