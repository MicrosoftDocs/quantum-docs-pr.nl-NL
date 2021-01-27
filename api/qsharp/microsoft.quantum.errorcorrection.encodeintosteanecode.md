---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Bewerking EncodeIntoSteaneCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 2f65423a17dafadd1f9f10a07335150dfc8bf886
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826193"
---
# <a name="encodeintosteanecode-operation"></a><span data-ttu-id="d158d-102">Bewerking EncodeIntoSteaneCode</span><span class="sxs-lookup"><span data-stu-id="d158d-102">EncodeIntoSteaneCode operation</span></span>

<span data-ttu-id="d158d-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d158d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d158d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d158d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d158d-105">Een coderings bewerking waarbij een niet-versleutelde Quantum wordt toegewezen aan een versleuteld Quantum REGI ster onder de Quantum code ⟦, 1, 3 ⟧ Steane.</span><span class="sxs-lookup"><span data-stu-id="d158d-105">An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="d158d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d158d-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="d158d-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d158d-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d158d-108">Een Qubit-REGI ster dat de niet-versleutelde Quantum status bevat</span><span class="sxs-lookup"><span data-stu-id="d158d-108">A qubit register which holds the an unencoded quantum state</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="d158d-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d158d-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d158d-110">Een Qubit-REGI ster dat in eerste instantie nul is en dat wordt toegevoegd aan het Quantum systeem zodat een coderings bewerking kan worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="d158d-110">A qubit register which is initially zero and which gets added to the quantum system so that an encoding operation can be performed</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="d158d-111">Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="d158d-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="d158d-112">Een Quantum registreert de status nadat het Steane-coderings programma is toegepast</span><span class="sxs-lookup"><span data-stu-id="d158d-112">A quantum register holding the state after the Steane encoder has been applied</span></span>

## <a name="see-also"></a><span data-ttu-id="d158d-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d158d-113">See Also</span></span>

- [<span data-ttu-id="d158d-114">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="d158d-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="d158d-115">Micro soft. Quantum. ErrorCorrection. SteaneCodeDecoder</span><span class="sxs-lookup"><span data-stu-id="d158d-115">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)