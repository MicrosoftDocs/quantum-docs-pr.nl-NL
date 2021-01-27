---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Bewerking EncodeIntoBitFlipCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 44034a864c946a7d3dbb21bad5ee500660709f1a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826683"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="a22af-102">Bewerking EncodeIntoBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="a22af-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="a22af-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a22af-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a22af-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a22af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a22af-105">Hiermee wordt gecodeerd in de [3, 1, 3]/⟦ 3, 1, 1 ⟧ bits-Flip code.</span><span class="sxs-lookup"><span data-stu-id="a22af-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="a22af-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a22af-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="a22af-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a22af-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a22af-108">Een REGI ster van fysieke qubits die de gegevens vertegenwoordigen die moeten worden beveiligd.</span><span class="sxs-lookup"><span data-stu-id="a22af-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="a22af-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a22af-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a22af-110">Een REGI ster van de hulp qubits in eerste instantie in de $ \ket {00} $-status die moet worden gebruikt bij het coderen van de gegevens die moeten worden beveiligd.</span><span class="sxs-lookup"><span data-stu-id="a22af-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="a22af-111">Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="a22af-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="a22af-112">De fysieke en hulp qubits die worden gebruikt in de code ring, weer gegeven als een logisch REGI ster.</span><span class="sxs-lookup"><span data-stu-id="a22af-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="a22af-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a22af-113">See Also</span></span>

- [<span data-ttu-id="a22af-114">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="a22af-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)