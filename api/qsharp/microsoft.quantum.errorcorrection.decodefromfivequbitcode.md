---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Bewerking DecodeFromFiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 77c5614684f416c7d2e12914ec6246d3ef7098fb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201101"
---
# <a name="decodefromfivequbitcode-operation"></a><span data-ttu-id="5491c-102">Bewerking DecodeFromFiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="5491c-102">DecodeFromFiveQubitCode operation</span></span>

<span data-ttu-id="5491c-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="5491c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="5491c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5491c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5491c-105">Decodeert de ⟦ van 5, 1, 3 en ⟧.</span><span class="sxs-lookup"><span data-stu-id="5491c-105">Decodes the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="5491c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5491c-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="5491c-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="5491c-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="5491c-108">Een matrix met qubits die de code ring logische status van 5 Qubit vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="5491c-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="5491c-109">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="5491c-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="5491c-110">Een Qubit-matrix van lengte 1 die de niet-versleutelde status in de eerste para meter weergeeft, samen met de hulp qubits in de tweede para meter.</span><span class="sxs-lookup"><span data-stu-id="5491c-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="5491c-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5491c-111">See Also</span></span>

- [<span data-ttu-id="5491c-112">Micro soft. Quantum. ErrorCorrection. FiveQubitCodeEncoder</span><span class="sxs-lookup"><span data-stu-id="5491c-112">Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [<span data-ttu-id="5491c-113">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="5491c-113">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)