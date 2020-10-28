---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Bewerking EncodeIntoFiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702507"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="84573-102">Bewerking EncodeIntoFiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="84573-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="84573-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="84573-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="84573-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84573-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84573-105">Codeert in de ⟦ van 5, 1, 3 en ⟧.</span><span class="sxs-lookup"><span data-stu-id="84573-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="84573-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="84573-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="84573-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="84573-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="84573-108">Een Qubit die een niet-gecodeerde status voor stelt.</span><span class="sxs-lookup"><span data-stu-id="84573-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="84573-109">Deze matrix `Qubit[]` heeft de lengte 1.</span><span class="sxs-lookup"><span data-stu-id="84573-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="84573-110">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="84573-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="84573-111">Een REGI ster met hulp qubits die wordt gebruikt om de gecodeerde status voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="84573-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="84573-112">Uitvoer: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="84573-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="84573-113">Een matrix met fysieke qubits van `LogicalRegister` het type dat de gecodeerde status opslaat.</span><span class="sxs-lookup"><span data-stu-id="84573-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="84573-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="84573-114">See Also</span></span>

- [<span data-ttu-id="84573-115">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="84573-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)