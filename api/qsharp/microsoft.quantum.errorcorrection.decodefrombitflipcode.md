---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Bewerking DecodeFromBitFlipCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 84cf83f24d02f261f1768e16390f83c9b294b759
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201152"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="b6f42-102">Bewerking DecodeFromBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="b6f42-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="b6f42-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b6f42-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b6f42-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b6f42-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b6f42-105">Decoderen van de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-Flip code.</span><span class="sxs-lookup"><span data-stu-id="b6f42-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="b6f42-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b6f42-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="b6f42-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="b6f42-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="b6f42-108">Een code blok van de bits-Flip-code.</span><span class="sxs-lookup"><span data-stu-id="b6f42-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="b6f42-109">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="b6f42-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="b6f42-110">Een tuple van de gegevens die zijn gecodeerd in het logische REGI ster en de hulp qubits die wordt gebruikt om de Syndrome aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="b6f42-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6f42-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b6f42-111">See Also</span></span>

- [<span data-ttu-id="b6f42-112">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="b6f42-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="b6f42-113">Micro soft. Quantum. ErrorCorrection. EncodeIntoBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="b6f42-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)