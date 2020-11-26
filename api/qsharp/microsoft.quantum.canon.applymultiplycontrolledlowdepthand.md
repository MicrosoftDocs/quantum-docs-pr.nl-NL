---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Bewerking ApplyMultiplyControlledLowDepthAnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209193"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="e7039-102">Bewerking ApplyMultiplyControlledLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="e7039-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="e7039-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e7039-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e7039-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7039-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7039-105">Implementeert een multi-beheerde Toffoli-Gate, ervan uitgaande dat de doel-Qubit 0 is geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="e7039-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="e7039-106">Bij de bewerking adjoint wordt ervan uitgegaan dat de doel-Qubit opnieuw wordt ingesteld op 0.</span><span class="sxs-lookup"><span data-stu-id="e7039-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="e7039-107">Vereist een RZ diepte van 1, terwijl het aantal helper-qubits exponentieel is in het aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="e7039-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="e7039-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e7039-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="e7039-109">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e7039-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e7039-110">Qubits beheren</span><span class="sxs-lookup"><span data-stu-id="e7039-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e7039-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e7039-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e7039-112">Doel-Qubit</span><span class="sxs-lookup"><span data-stu-id="e7039-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="e7039-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e7039-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

