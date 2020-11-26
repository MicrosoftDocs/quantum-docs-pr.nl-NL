---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Bewerking EncodeIntoBitFlipCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b27759caba3c5dd363dbdf24d6e5de76870173cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200948"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="557b7-102">Bewerking EncodeIntoBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="557b7-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="557b7-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="557b7-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="557b7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="557b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="557b7-105">Hiermee wordt gecodeerd in de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bits-Flip code.</span><span class="sxs-lookup"><span data-stu-id="557b7-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="557b7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="557b7-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="557b7-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="557b7-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="557b7-108">Een REGI ster van fysieke qubits die de gegevens vertegenwoordigen die moeten worden beveiligd.</span><span class="sxs-lookup"><span data-stu-id="557b7-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="557b7-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="557b7-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="557b7-110">Een REGI ster van de hulp qubits in eerste instantie in de $ \ket {00} $-status die moet worden gebruikt bij het coderen van de gegevens die moeten worden beveiligd.</span><span class="sxs-lookup"><span data-stu-id="557b7-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="557b7-111">Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="557b7-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="557b7-112">De fysieke en hulp qubits die worden gebruikt in de code ring, weer gegeven als een logisch REGI ster.</span><span class="sxs-lookup"><span data-stu-id="557b7-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="557b7-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="557b7-113">See Also</span></span>

- [<span data-ttu-id="557b7-114">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="557b7-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)