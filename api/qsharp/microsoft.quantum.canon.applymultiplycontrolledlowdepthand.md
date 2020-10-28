---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Bewerking ApplyMultiplyControlledLowDepthAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 6900f9b0f014fba28ae73a70f180f3e4696900cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705188"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="f0d00-102">Bewerking ApplyMultiplyControlledLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="f0d00-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="f0d00-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0d00-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0d00-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0d00-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0d00-105">Implementeert een multi-beheerde Toffoli-Gate, ervan uitgaande dat de doel-Qubit 0 is geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="f0d00-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="f0d00-106">Bij de bewerking adjoint wordt ervan uitgegaan dat de doel-Qubit opnieuw wordt ingesteld op 0.</span><span class="sxs-lookup"><span data-stu-id="f0d00-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="f0d00-107">Vereist een RZ diepte van 1, terwijl het aantal helper-qubits exponentieel is in het aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="f0d00-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f0d00-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f0d00-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="f0d00-109">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f0d00-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f0d00-110">Qubits beheren</span><span class="sxs-lookup"><span data-stu-id="f0d00-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f0d00-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f0d00-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f0d00-112">Doel-Qubit</span><span class="sxs-lookup"><span data-stu-id="f0d00-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0d00-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0d00-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

